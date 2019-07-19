#
# Copyright (C) 2014 Bernd Ocklin <bernd@vyacht.net>
#
# This file is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
# 
# For the license of the actually jquery please check subfolders.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=bootstrap
PKG_VERSION:=3.3.6
PKG_RELEASE:=dist

PKG_SOURCE:=v$(PKG_VERSION).zip
PKG_SOURCE_URL:=https://github.com/twbs/bootstrap/archive
PKG_MD5SUM:=4a7e3a760d3625dcc8010b26781995d7

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
PKG_DIST_DIR:=$(PKG_BUILD_DIR)/dist

include $(INCLUDE_DIR)/package.mk

define Package/bootstrap
	CATEGORY:=VYACHT
	TITLE:=bootstrap
	MAINTAINER:=Bernd Ocklin <bernd@vyacht.net>
endef

define Package/bootstrap/description
  Package for bootstrap dependencies.
endef

define Build/Prepare
	unzip $(DL_DIR)/$(PKG_SOURCE) -d $(BUILD_DIR)
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/bootstrap/install
	$(INSTALL_DIR) $(1)/www/bootstrap
	$(INSTALL_DIR) $(1)/www/bootstrap/css
	$(INSTALL_DIR) $(1)/www/bootstrap/fonts
	$(INSTALL_DIR) $(1)/www/bootstrap/js
	$(INSTALL_DATA) $(PKG_DIST_DIR)/css/* $(1)/www/bootstrap/css/
	$(INSTALL_DATA) $(PKG_DIST_DIR)/fonts/* $(1)/www/bootstrap/fonts/
	$(INSTALL_DATA) $(PKG_DIST_DIR)/js/* $(1)/www/bootstrap/js/
endef

$(eval $(call BuildPackage,bootstrap))
