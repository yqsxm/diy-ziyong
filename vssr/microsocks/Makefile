include $(TOPDIR)/rules.mk

PKG_NAME:=microsocks
PKG_VERSION=1.0.1
PKG_RELEASE:=1

PKG_MAINTAINER:=lean
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/rofl0r/microsocks.git
PKG_SOURCE_VERSION:=6824373d6fc2a2ecb047c64175b6f4fcc90291f29c68fb17fdda692c4c0249cb

PKG_SOURCE_SUBDIR:=$(PKG_NAME)
PKG_SOURCE:=$(PKG_NAME).$(PKG_VERSION).$(PKG_RELEASE).tar.gz
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_SOURCE_SUBDIR)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/microsocks
	SECTION:=net
	CATEGORY:=Network
	TITLE:=microsocks for OpenWRT
	DEPENDS:=
endef

define Package/microsocks/description
	microsocks is a Tiny Proxy in C.
endef

define Package/microsocks/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/microsocks $(1)/usr/bin/microsocks
endef

$(eval $(call BuildPackage,microsocks))
