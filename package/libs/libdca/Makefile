#
# Copyright (C) 2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=libdca
PKG_VERSION:=0.0.5
PKG_RELEASE:=1

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_URL:=http://download.videolan.org/pub/videolan/libdca/0.0.5/
PKG_MD5SUM:=dab6b2795c66a82a6fcd4f8343343021
PKG_MAINTAINER:=SunKe <sunke@duotin.com>

PKG_INSTALL:=1
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/libdca
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=libdca to support dts decoder
  URL:=http://www.videolan.org/
endef

CONFIGURE_ARGS += \

define Build/InstallDev
	$(INSTALL_DIR) $(1)
	$(CP) $(PKG_INSTALL_DIR)/* $(1)/
endef

define Package/libdca/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libdca.so.* $(1)/usr/lib/
endef

$(eval $(call BuildPackage,libdca))
