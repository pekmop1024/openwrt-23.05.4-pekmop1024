# openwrt-23.05.4-pekmop1024
Packages built for GL.inet GL-E750 that runs vanilla OpenWrt 23.05.4

## Current packages
* **dnsmasq-full** with enabled ipset support (needed for domain-based ipsets used in mwan3 policy-based routing)
* **gl-e750-mcu** ([details](https://github.com/pekmop1024/gl-e750-mcu))
* **gl-e750-mcu-oled** ([details](https://github.com/pekmop1024/gl-e750-mcu-oled))
* **luci-app-3ginfo-lite** ([details](https://github.com/pekmop1024/luci-app-3ginfo-lite))

## Add repo to opkg
```
grep -q pekmop1024 /etc/opkg/customfeeds.conf || echo 'src/gz pekmop1024 https://github.com/pekmop1024/openwrt-23.05.4-pekmop1024/raw/main' >> /etc/opkg/customfeeds.conf
wget https://github.com/pekmop1024/openwrt-23.05.4-pekmop1024/raw/main/pekmop1024-repo.pub -O /tmp/pekmop1024-repo.pub
opkg-key add /tmp/pekmop1024-repo.pub
opkg update
```
