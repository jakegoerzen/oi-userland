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

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		celestia
COMPONENT_VERSION=	1.6.2.2
COMPONENT_SUMMARY=	Real-time 3D visualization of space.
COMPONENT_PROJECT_URL=	https://celestia.space
COMPONENT_FMRI=		image/celestia
COMPONENT_CLASSIFICATION=	Applications/Graphics and Imaging
COMPONENT_SRC_NAME=	Celestia
COMPONENT_SRC=          $(COMPONENT_SRC_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=      $(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH=	sha256:d4d3bccf104a9beaf4bedb58e407172555b67113bbff3e0134d4a831d747419b
COMPONENT_ARCHIVE_URL=  https://github.com/CelestiaProject/Celestia/archive/refs/tags/1.6.2.2.tar.gz
COMPONENT_LICENSE=	GPLv2.0
COMPONENT_LICENSE_FILE=	COPYING

TEST_TARGET= $(NO_TESTS)
include $(WS_MAKE_RULES)/common.mk

COMPONENT_PRE_CONFIGURE_ACTION = cd $(COMPONENT_SRC) && libtoolize && autoreconf -f

CONFIGURE_OPTIONS += --with-glut

# Auto-generated dependencies
