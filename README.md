# OpenWrt-Create-Hello-Package

Create a custom package for OpenWrt.

## How To

	cd ~
	git clone https://github.com/JiapengLi/OpenWrt-Create-Hello-Package.git
	cd openwrt/trunk
	./scripts/feeds update -a
	./scripts/feeds install -a
	cd feeds/packages
	patch -p1 < ~/OpenWrt-Create-Hello-Package/openwrt-create-hello-package.patch
	./scripts/feeds update -i
	./scripts/feeds install hello
	
	make menuconfig
	// choose the right platform
	// Select hello in Utilities --> hello

	make

## Build Single Package

	make package/hello/compile V=s
	make package/hello/install V=s
	make package/index

## Useful Links

(Write and cmopile a simple package for OpenWrt)[http://www.gargoyle-router.com/wiki/doku.php?id=openwrt_coding]
(Create Package)[http://wiki.openwrt.org/doc/devel/packages]
(Build Single Package)[http://wiki.openwrt.org/doc/howtobuild/single.package]
(Building your own package for OpenWRT)[http://vivekian2.wordpress.com/2007/03/28/building-your-own-package-for-openwrt/]  