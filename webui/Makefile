#2016 Copyright (c) Seeed Technology Inc.  All right reserved.
#	Author:Baozhu Zuo
#	Permission is hereby granted, free of charge, to any person obtaining a copy
#of this software and associated documentation files (the "Software"), to deal
#in the Software without restriction, including without limitation the rights
#to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
#copies of the Software, and to permit persons to whom the Software is
#furnished to do so, subject to the following conditions:
#The above copyright notice and this permission notice shall be included in
#all copies or substantial portions of the Software.
#THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
#IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
#FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
#AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
#LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
#OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
#THE SOFTWARE.
#
include $(TOPDIR)/rules.mk

PKG_NAME:=webui
PKG_VERSION:=0.0.1
PKG_RELEASE:=$(PKG_SOURCE_VERSION)

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/respeaker/respeaker_wifi_webUI.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)
PKG_SOURCE_VERSION:=20bc2048724ee5969eda27172853048d590e37d9
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz
PKG_MAINTAINER:=Baozhu Zuo <zuobaozhu@gmail.com>


PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)


include $(INCLUDE_DIR)/package.mk
define Package/webui
	SECTION:=utils
	CATEGORY:=ReSpeaker
	TITLE:=respeaker webui
endef

define Build/Configure
endef
define Build/Compile
endef
define Package/webui/install
	mkdir -p $(1)/www
	$(CP) $(PKG_BUILD_DIR)/login.html $(1)/www/

	mkdir -p $(1)/www/js
	$(CP) $(PKG_BUILD_DIR)/js/*   $(1)/www/js/

	mkdir -p $(1)/www/img
	$(CP) $(PKG_BUILD_DIR)/img/*   $(1)/www/img/

	mkdir -p $(1)/www/css
	$(CP) $(PKG_BUILD_DIR)/css/*   $(1)/www/css/
endef

$(eval $(call BuildPackage,webui))
