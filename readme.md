##wifi setup & ssh

####vi /etc/network/interfaces
```
auto lo
iface lo inet loopback
iface eth0 inet dhcp

allow-hotplug wlan0
iface wlan0 inet dhcp
wpa-conf /etc/wpa_supplicant/wpa_supplicant.conf
iface default inet dhcp
```

####After changing the file issue (as root):

```
/etc/init.d/networking restart
wpa_passphrase WIFI_NAME PASSWORD >> /etc/wpa_supplicant/wpa_supplicant.conf
```

