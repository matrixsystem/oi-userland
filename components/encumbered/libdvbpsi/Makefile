#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"), version 1.0.
# You may only use this file in accordance with the terms of version
# 1.0 of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source.  A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2015 Alexander Pyhalov
#

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME= libdvbpsi
COMPONENT_VERSION= 1.3.1
COMPONENT_FMRI = library/video/libdvbpsi
COMPONENT_CLASSIFICATION = System/Multimedia Libraries
COMPONENT_SUMMARY= A simple library designed for decoding and generation of MPEG TS and DVB PSI tables
COMPONENT_SRC= $(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE= $(COMPONENT_SRC).tar.bz2
COMPONENT_ARCHIVE_HASH= \
  sha256:d68367afd5ad8e6ebca813e7958a3ceb9743b421adb4265eceeb6a3511c84420
COMPONENT_ARCHIVE_URL= \
  http://download.videolan.org/pub/libdvbpsi/$(COMPONENT_VERSION)/$(COMPONENT_ARCHIVE)
COMPONENT_PROJECT_URL = http://www.videolan.org/developers/libdvbpsi.html
COMPONENT_LICENSE = LGPLv2.1
COMPONENT_LICENSE_FILE = COPYING

include $(WS_MAKE_RULES)/encumbered.mk
include $(WS_MAKE_RULES)/prep.mk
include $(WS_MAKE_RULES)/configure.mk
include $(WS_MAKE_RULES)/ips.mk

LDFLAGS += -lsocket -lnsl

build: $(BUILD_32_and_64)

install: $(INSTALL_32_and_64)

test: $(NO_TESTS)

# Auto-generated dependencies
REQUIRED_PACKAGES += system/library
