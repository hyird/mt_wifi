#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=mt_wifi
PKG_VERSION:=1
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/mt_wifi-mt7615-dbdc
  SECTION:=net
  CATEGORY:=Network
  TITLE:=MTK wifi AP config
  DEPENDS:=@TARGET_ramips +wireless-tools
  SUBMENU:=Wireless
endef

define Package/mt_wifi-mt7615-dual
  SECTION:=net
  CATEGORY:=Network
  TITLE:=MTK wifi AP config
  DEPENDS:=@TARGET_ramips +wireless-tools
  SUBMENU:=Wireless
endef

define Package/mt_wifi-mt7603-mt7612
  SECTION:=net
  CATEGORY:=Network
  TITLE:=MTK wifi AP config
  DEPENDS:=@TARGET_ramips +wireless-tools
  SUBMENU:=Wireless
endef

define Package/mt_wifi-mt7603-mt7615
  SECTION:=net
  CATEGORY:=Network
  TITLE:=MTK wifi AP config
  DEPENDS:=@TARGET_ramips +wireless-tools
  SUBMENU:=Wireless
endef

define Package/mt_wifi-mt7615-dbdc/description
  MT_WiFi auto config for mt7603/mt7612/mt7615 chips
endef

define Package/mt_wifi-mt7615-dual/description
  MT_WiFi auto config for mt7603/mt7612/mt7615 chips
endef

define Package/mt_wifi-mt7603-mt7612/description
  MT_WiFi auto config for mt7603/mt7612/mt7615 chips
endef

define Package/mt_wifi-mt7603-mt7615/description
  MT_WiFi auto config for mt7603/mt7612/mt7615 chips
endef

define Build/Compile
endef

define Package/mt_wifi-mt7615-dbdc/install
	$(INSTALL_DIR) $(1)/etc/init.d/
	$(INSTALL_DIR) $(1)/lib/wifi/
	$(INSTALL_DIR) $(1)/etc/wireless/mt7615/
	$(INSTALL_DIR) $(1)/etc_ro/Wireless/RT2860AP/
	$(INSTALL_DIR) $(1)/lib/preinit/

	$(INSTALL_BIN) ./files/dbdc.l1profile.dat $(1)/etc/wireless/l1profile.dat
	$(INSTALL_BIN) ./files/mt7615.1.2G.dat $(1)/etc/wireless/mt7615/
	$(INSTALL_BIN) ./files/mt7615.1.5G.dat $(1)/etc/wireless/mt7615/

	$(INSTALL_BIN) ./files/SingleSKU.dat $(1)/etc_ro/Wireless/RT2860AP/
	$(INSTALL_BIN) ./files/SingleSKU_BF.dat $(1)/etc_ro/Wireless/RT2860AP/
	$(INSTALL_BIN) ./files/mt7615.lua $(1)/lib/wifi
	$(INSTALL_BIN) ./files/firmware.sh $(1)/etc/init.d/
	$(INSTALL_BIN) ./files/82_load_wifi.sh $(1)/lib/preinit/
endef

define Package/mt_wifi-mt7615-dual/install
	$(INSTALL_DIR) $(1)/etc/init.d/
	$(INSTALL_DIR) $(1)/lib/wifi/
	$(INSTALL_DIR) $(1)/etc/wireless/mt7615/
	$(INSTALL_DIR) $(1)/etc_ro/Wireless/RT2860AP/
	$(INSTALL_DIR) $(1)/lib/preinit/

	$(INSTALL_BIN) ./files/7615.l1profile.dat $(1)/etc/wireless/l1profile.dat
	$(INSTALL_BIN) ./files/mt7615.2G.dat $(1)/etc/wireless/mt7615/
	$(INSTALL_BIN) ./files/mt7615.5G.dat $(1)/etc/wireless/mt7615/

	$(INSTALL_BIN) ./files/SingleSKU.dat $(1)/etc_ro/Wireless/RT2860AP/
	$(INSTALL_BIN) ./files/SingleSKU_BF.dat $(1)/etc_ro/Wireless/RT2860AP/
	$(INSTALL_BIN) ./files/mt7615.lua $(1)/lib/wifi
	$(INSTALL_BIN) ./files/firmware.sh $(1)/etc/init.d/
	$(INSTALL_BIN) ./files/82_load_wifi.sh $(1)/lib/preinit/
endef

define Package/mt_wifi-mt7603-mt7612/install
	$(INSTALL_DIR) $(1)/etc/init.d/
	$(INSTALL_DIR) $(1)/lib/wifi/
	$(INSTALL_DIR) $(1)/etc/wireless/mt7615/
	$(INSTALL_DIR) $(1)/etc_ro/Wireless/RT2860AP/
	$(INSTALL_DIR) $(1)/lib/preinit/

	$(INSTALL_BIN) ./files/dbdc.l1profile.dat $(1)/etc/wireless/l1profile.dat
	$(INSTALL_BIN) ./files/mt7615.1.2G.dat $(1)/etc/wireless/mt7615/
	$(INSTALL_BIN) ./files/mt7615.1.5G.dat $(1)/etc/wireless/mt7615/

	$(INSTALL_BIN) ./files/SingleSKU.dat $(1)/etc_ro/Wireless/RT2860AP/
	$(INSTALL_BIN) ./files/SingleSKU_BF.dat $(1)/etc_ro/Wireless/RT2860AP/
	$(INSTALL_BIN) ./files/mt7615.lua $(1)/lib/wifi
	$(INSTALL_BIN) ./files/firmware.sh $(1)/etc/init.d/
	$(INSTALL_BIN) ./files/82_load_wifi.sh $(1)/lib/preinit/
endef

define Package/mt_wifi-mt7603-mt7615/install
	$(INSTALL_DIR) $(1)/etc/init.d/
	$(INSTALL_DIR) $(1)/lib/wifi/
	$(INSTALL_DIR) $(1)/etc/wireless/mt7615/
	$(INSTALL_DIR) $(1)/etc_ro/Wireless/RT2860AP/
	$(INSTALL_DIR) $(1)/lib/preinit/

	$(INSTALL_BIN) ./files/7603_7615-l1profile.dat $(1)/etc/wireless/l1profile.dat
	$(INSTALL_BIN) ./files/mt7603.dat $(1)/etc/wireless/mt7615/mt7615.1.dat
	$(INSTALL_BIN) ./files/mt7615.dat $(1)/etc/wireless/mt7615/mt7615.2.dat

	$(INSTALL_BIN) ./files/SingleSKU.dat $(1)/etc_ro/Wireless/RT2860AP/
	$(INSTALL_BIN) ./files/SingleSKU_BF.dat $(1)/etc_ro/Wireless/RT2860AP/
	$(INSTALL_BIN) ./files/mt7615.lua $(1)/lib/wifi
	$(INSTALL_BIN) ./files/firmware.sh $(1)/etc/init.d/
	$(INSTALL_BIN) ./files/82_load_wifi.sh $(1)/lib/preinit/
endef

$(eval $(call BuildPackage,mt_wifi-mt7615-dbdc))
$(eval $(call BuildPackage,mt_wifi-mt7615-dual))
$(eval $(call BuildPackage,mt_wifi-mt7603-mt7612))
$(eval $(call BuildPackage,mt_wifi-mt7603-mt7615))

