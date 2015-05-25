# initramfs-dhcp-resolv.conf
Simple initramfs hooks and scripts for enabling dhcp networking with domain resolving.

###Limited networking support

These scripts has hardcoded default interface dhcp-support, and does not parse the kernel commandline "ip" variable.
If you want to extend it's functionalities, reference <a href="https://github.com/opinsys/ltsp/tree/master/client/Debian/share/initramfs-tools">ltsp initramfs</a> and nfs inside /usr/share/initramfs-tools/.

###Curl support

I wrote these hooks and scripts to automagically grab cryptsetup keys from an HTTPS server over an IPSEC tunnel, and since Busybox wget implementation doesn't support the HTTPS scheme, I've included curl.
If you don't need it, remove or chmod -x <a href="hooks/curl">hooks/curl</a>.
