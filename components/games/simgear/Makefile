#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL)". You may
# only use this file in accordance with the terms of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source. A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright (c) 2021 Jake Goerzen

BUILD_BITS=	32_and_64
BUILD_STYLE=	cmake

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		simgear
COMPONENT_VERSION=	2020.3.13
COMPONENT_PROJECT_URL=	https://www.flightgear.org
COMPONENT_SUMMARY=	FightGear - an open-source flight simulator.
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.bz2
COMPONENT_ARCHIVE_HASH=	\
	sha256:dc09906fda8b1810fe2cb22b5f5171d208ba901c5b9d390bad6d1f3fd66c51e8
COMPONENT_ARCHIVE_URL=	https://sourceforge.net/projects/flightgear/files/release-2020.3/$(COMPONENT_ARCHIVE)
COMPONENT_FMRI =	games/flightgear
COMPONENT_LICENSE=	LGPL
COMPONENT_LICENSE_FILE=	COPYING
COMPONENT_CLASSIFICATION =	Application/Games

include $(WS_MAKE_RULES)/common.mk

CMAKE_OPTIONS += -DCMAKE_CXX_FLAGS=-std=c++11
#CMAKE_OPTIONS += -DSIMGEAR_HEADLESS=ON

# Auto-generated dependencies
