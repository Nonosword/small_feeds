include $(TOPDIR)/rules.mk

PKG_NAME:=ddns-scripts-dnspod-cn
PKG_RELEASE:=1
PKG_LICENSE:=MIT
PKG_MAINTAINER:=Nonosword

include $(INCLUDE_DIR)/package.mk

define Package/ddns-scripts-dnspod-cn
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=IP Addresses and Names
  TITLE:=Dynamic DNS scripts extension for DNSPod China
  PKGARCH:=all
  DEPENDS:=+ddns-scripts +curl +ca-bundle
endef

define Package/ddns-scripts-dnspod-cn/description
 Dynamic DNS provider extension for DNSPod China (dnspod.cn)
 for ddns-scripts / luci-app-ddns.
endef

define Build/Compile
endef

define Package/ddns-scripts-dnspod-cn/install
	$(INSTALL_DIR) $(1)/usr/share/ddns/default
	$(INSTALL_DIR) $(1)/usr/lib/ddns

	$(INSTALL_DATA) ./files/usr/share/ddns/default/dnspod.cn.json $(1)/usr/share/ddns/default/
	$(INSTALL_BIN) ./files/usr/lib/ddns/update_dnspod_cn.sh $(1)/usr/lib/ddns/
endef

$(eval $(call BuildPackage,ddns-scripts-dnspod-cn))
