#
# Copyright (C) 2009 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
# $Id: Makefile 15321 2009-04-21 11:38:28Z nico $

include $(TOPDIR)/rules.mk

PKG_NAME:=xf86-input-tslib
PKG_RELEASE:=1.1
PKG_VERSION:=0.0.5

PKG_SOURCE_URL:=http://www.pengutronix.de/software/xf86-input-tslib/download/
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_BUILD_DIR=$(BUILD_DIR)/Xorg/$(_CATEGORY)/$(PKG_NAME)-$(PKG_VERSION)/
PKG_MD5SUM:=4231b517d216e9f80ba66f13a0f30afd
PKG_BUILD_DEPENDS:=randrproto inputproto xproto
PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk

define Package/xf86-input-tslib
  SECTION:=xorg-driver
  CATEGORY:=Xorg
  SUBMENU:=driver
  DEPENDS:=+xserver-xorg +tslib
  TITLE:=xf86-input-tslib
  URL:=http://www.pengutronix.de/software/xf86-input-tslib/
endef

define Package/xf86-input-tslib/install
	$(INSTALL_DIR) $(1)/usr/lib/xorg/modules/input
	$(INSTALL_DATA) \
		$(PKG_INSTALL_DIR)/usr/lib/xorg/modules/input/tslib_drv.so \
		$(1)/usr/lib/xorg/modules/input/
endef

$(eval $(call BuildPackage,xf86-input-tslib))
