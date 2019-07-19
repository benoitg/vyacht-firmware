#
# Copyright (C) 2014 Bernd Ocklin <bernd@vyacht.net>
#
# This file is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
# 
# For the license of the actually jquery please check subfolders.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=vy-instrumentpanel
PKG_VERSION:=0.0.1
PKG_RELEASE:=1

#PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tgz

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/vyacht/instrumentpanel.git
PKG_MIRROR_HASH:=05c2583b7279bf05a4e8ae93afade4aa11dce9151d0bd05ba54fd9ed083f1125
PKG_SOURCE_DATE:=2016-04-06
PKG_SOURCE_VERSION:=34fed778b899c6fbb3dc25b995511999d6906718

include $(INCLUDE_DIR)/package.mk

define Package/vy-instrumentpanel
	CATEGORY:=VYACHT
  DEPENDS:=+uhttpd +font-awesome +bootstrap
  TITLE:=SignalK Instrumentpanel
	MAINTAINER:=Bernd Ocklin <bernd@vyacht.net>
endef

define Package/vy-instrumentpanel/description
  Package for SignalK instrument panel dependencies.
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/vy-instrumentpanel/install
	$(INSTALL_DIR) $(1)/www
	$(INSTALL_DIR) $(1)/www/dist
	$(INSTALL_DIR) $(1)/www/dist/css
	$(INSTALL_DIR) $(1)/www/dist/fonts
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/index.html $(1)/www/instrumentpanel.html
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/dist/ui.js $(1)/www/dist/ui.js
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/dist/vendor.js $(1)/www/dist/vendor.js
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/dist/css/bootstrap.min.css $(1)/www/dist/css/bootstrap.min.css
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/dist/css/font-awesome.css $(1)/www/dist/css/font-awesome.css
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/dist/fonts/fontawesome-webfont.eot $(1)/www/dist/fonts/fontawesome-webfont.eot
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/dist/fonts/fontawesome-webfont.svg $(1)/www/dist/fonts/fontawesome-webfont.svg
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/dist/fonts/fontawesome-webfont.ttf $(1)/www/dist/fonts/fontawesome-webfont.ttf
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/dist/fonts/fontawesome-webfont.woff $(1)/www/dist/fonts/fontawesome-webfont.woff
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/dist/fonts/fontawesome-webfont.woff2 $(1)/www/dist/fonts/fontawesome-webfont.woff2
	$(INSTALL_DATA) $(PKG_BUILD_DIR)/dist/fonts/FontAwesome.otf $(1)/www/dist/fonts/FontAwesome.otf
endef

$(eval $(call BuildPackage,vy-instrumentpanel))
