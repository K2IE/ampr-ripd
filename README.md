This project can be used with the OpenWRT SDK to generate a package for ampr-ripd.

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
