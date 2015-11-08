#
# Copyright (C) 2006-2014 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=jsoncpp
PKG_VERSION:=0.10.5
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
#PKG_SOURCE_URL:=https://s3.amazonaws.com/json-c_releases/releases/
#PKG_MD5SUM:=3ca4bbb881dfc4017e8021b5e0a8c491

#PKG_LICENSE:=MIT
#PKG_LICENSE_FILES:=COPYING

PKG_FIXUP:=autoreconf
PKG_INSTALL:=1

PKG_MAINTAINER:=Felix Fietkau <nbd@openwrt.org>

include $(INCLUDE_DIR)/package.mk

TARGET_CFLAGS += $(FPIC)

define Package/libjsoncpp
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=jsoncpp
#  URL:=http://oss.metaparadigm.com/json-c/
endef

define Package/libjsoncpp/description
 This package contains a library for javascript object notation backends.
endef

define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/include
	$(CP) $(PKG_INSTALL_DIR)/usr/local/include/json $(1)/usr/include/
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/local/lib/libjsoncpp.a $(1)/usr/lib/
	$(INSTALL_DIR) $(1)/usr/lib/pkgconfig
	$(CP) $(PKG_INSTALL_DIR)/usr/local/lib/pkgconfig/jsoncpp.pc $(1)/usr/lib/pkgconfig/
endef

define Package/libjsoncpp/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/local/lib/libjsoncpp.* $(1)/usr/lib/
endef

$(eval $(call BuildPackage,libjsoncpp))
