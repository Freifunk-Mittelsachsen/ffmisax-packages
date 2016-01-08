include $(TOPDIR)/rules.mk

PKG_NAME:=ffwdh-bench
PKG_VERSION:=1
PKG_RELEASE:=1

PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/ffwdh-bench
  SECTION:=net
  CATEGORY:=Libraries
  TITLE:=FFWDH Benchmark tool for ipv6 link local tests
  DEPENDS:=+gluon-core
endef

define Package/ffwdh-bench/description
    Create a server on port 10100 and on connect sends default 10MB of zeros with 10kb chunk size
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	$(CP) ./src/* $(PKG_BUILD_DIR)/
endef

define Build/Configure
endef

define Build/Compile
	CFLAGS="$(TARGET_CFLAGS)" CPPFLAGS="$(TARGET_CPPFLAGS)" $(MAKE) -C $(PKG_BUILD_DIR) $(TARGET_CONFIGURE_OPTS)
endef

define Package/ffwdh-bench/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/ffwdh-bench $(1)/usr/bin/
endef

$(eval $(call BuildPackage,ffwdh-bench))
