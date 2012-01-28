# 
# Copyright (C) 2011 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=usbrelay
PKG_VERSION:=0.01
PKG_RELEASE:=1

PKG_BUILD_DIR:=$(BUILD_DIR)/usbrelay

include $(INCLUDE_DIR)/package.mk

define Package/usbrelay
  SECTION:=utils
  CATEGORY:=Utilities
  DEPENDS:=+libusb
  TITLE:=usbrelay
endef

define Package/usbrelay/description
 usbRelay
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	$(CP) ./src/* $(PKG_BUILD_DIR)/
endef

define Package/usbrelay/install
	$(INSTALL_DIR) $(1)/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/usbrelay $(1)/sbin/
endef

$(eval $(call BuildPackage,usbrelay))
