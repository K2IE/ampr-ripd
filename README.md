This project can be used with the OpenWRT SDK to generate a package for ampr-ripd.  It is intended for use only by licensed amateur radio operators.

Before installing the package, export the following variables (examples only!):

```
amprhost='44.44.44.1'
amprmask='255.255.255.0'
amprnet='44.44.44.0'
```

Then:

```
opkg update
opkg install ampr-ripd_2.4-1_{your architecture}.ipk
```

Other things to do include:
```
Edit /etc/ampr-ripd.conf.
Use the Luci GUI to validate the Firewall - Zone Settings.
Add a Firewall - Traffic rule to allow IPIP to "this device".
Add a firewall - Traffic rule to allow Net44 ICMP Echo Request from amprwan
 to amprlan as well as from amprwan to "this device".
/etc/init.d/ampr-ripd restart
```

After a short while:
```
ip route show table 44
```

If everything is working properly, you should see many tunnel routes to other 44.x networks.

73 de K2IE
