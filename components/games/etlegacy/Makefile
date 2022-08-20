#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"). You may
# only use this file in accordance with the terms of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source. A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2022 Jake Goerzen
#

# need 32 Bit for compatibility with ET 2.60b
BUILD_BITS= 32
BUILD_STYLE= cmake

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		etlegacy
COMPONENT_VERSION=	2.80.2
COMPONENT_SUMMARY=	A free multiplayer first-person shooter.
COMPONENT_PROJECT_URL=	https://www.etlegacy.com
COMPONENT_FMRI=		games/etlegacy
COMPONENT_CLASSIFICATION=	Applications/Games
COMPONENT_SRC_NAME=	etlegacy
COMPONENT_SRC=          $(COMPONENT_SRC_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=      $(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH=	sha256:1b22c131d6c122b38a88306d8dc81ea0135a0f60f599d6f871a175b311b00409
COMPONENT_ARCHIVE_URL=  https://github.com/etlegacy/etlegacy/archive/refs/tags/v2.80.2.tar.gz
COMPONENT_LICENSE=	GPLv2.0
COMPONENT_LICENSE_FILE=	COPYING

TEST_TARGET= $(NO_TESTS)
include $(WS_MAKE_RULES)/common.mk

LDFLAGS += -lGL -lGLEW -lsocket -lnsl -L/usr/lib/libjpeg8-turbo/lib -R/usr/lib/libjpeg8-turbo/lib -lturbojpeg

# get the bundled libs
COMPONENT_PREP_ACTION += cd $(COMPONENT_SRC) && git clone https://github.com/etlegacy/etlegacy-libs.git libs

CMAKE_OPTIONS += -DCMAKE_C_FLAGS=-fPIC
#CMAKE_OPTIONS += -DGLEW_INCLUDE_PATH=/usr/include
CMAKE_OPTIONS += -DBUNDLED_LIBS=1
CMAKE_OPTIONS += -DBUNDLED_SDL=0
CMAKE_OPTIONS += -DBUNDLED_ZLIB=0
CMAKE_OPTIONS += -DBUNDLED_MINIZIP=1
CMAKE_OPTIONS += -DBUNDLED_CURL=0
CMAKE_OPTIONS += -DBUNDLED_JPEG=1
CMAKE_OPTIONS += -DBUNDLED_LUA=1
CMAKE_OPTIONS += -DBUNDLED_OGG_VORBIS=0
CMAKE_OPTIONS += -DBUNDLED_THEORA=0
CMAKE_OPTIONS += -DBUNDLED_OPENAL=0
CMAKE_OPTIONS += -DBUNDLED_GLEW=1
CMAKE_OPTIONS += -DBUNDLED_FREETYPE=0
CMAKE_OPTIONS += -DBUNDLED_PNG=0
CMAKE_OPTIONS += -DBUNDLED_SQLITE3=0
CMAKE_OPTIONS += -DBUNDLED_OPENSSL=0
CMAKE_OPTIONS += -DBUNDLED_WOLFSSL=0

# Auto-generated dependencies
REQUIRED_PACKAGES += $(GCC_RUNTIME_PKG)
REQUIRED_PACKAGES += $(GXX_RUNTIME_PKG)
REQUIRED_PACKAGES += image/library/libjpeg8-turbo
REQUIRED_PACKAGES += library/zlib
