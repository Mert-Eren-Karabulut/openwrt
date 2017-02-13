# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.

include $(TOPDIR)/rules.mk

PKG_NAME:=hello-ocp
PKG_RELEASE:=1

PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/hello-ocp
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Hello world
  MAINTAINER:=Abylay Ospan <aospan@jokersys.com>
endef

define Package/hello-ocp/description
  This is hello world example
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	$(CP) ./src/* $(PKG_BUILD_DIR)/
endef

define Package/hello-ocp/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/hello-ocp $(1)/usr/bin/hello-ocp
endef

$(eval $(call BuildPackage,hello-ocp))
