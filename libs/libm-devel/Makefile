#
# Copyright (C) 2013 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=libm-dev
PKG_VERSION:=0.999
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/libm-dev
  SECTION:=devel
  CATEGORY:=Development
  SUBMENU:=Libraries
  TITLE:=libm-dev
  DEPENDS:=
endef

define Package/libm-dev/description
  contains libm.a
endef

GCC_VERSION=$(grep -e "PKG_VERSION:=" ../../devel/gcc/Makefile|cut -d "=" -f 2)

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Compile
endef

define Build/Install
endef

define Package/libm-dev/install
	$(INSTALL_DIR) $(1)/usr/lib/gcc/$(REAL_GNU_TARGET_NAME)/$(GCC_VERSION)
	$(CP) $(STAGING_DIR_ROOT)/lib/libm.a $(1)/usr/lib/gcc/$(REAL_GNU_TARGET_NAME)/$(GCC_VERSION)/
endef

$(eval $(call BuildPackage,libm-dev))
