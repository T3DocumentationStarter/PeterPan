.. include:: ../Includes.txt

=========
About VPN
=========

Investigate
===========

-  search, https://www.startpage.com/do/dsearch?query=ubuntu+route+ip+traffic+through+vpn
-  Routing All Traffic Through a VPN Gateway on Linux (networking, vpn):
   https://sweetcode.io/routing-all-traffic-through-a-vpn-gateway-on-linux/


How-to
======

Following https://sweetcode.io/routing-all-traffic-through-a-vpn-gateway-on-linux/

Assuming VPN ip is 10.1.1.1

Find default route::

   ➜  route

   Kernel-IP-Routentabelle
   Ziel            Router          Genmask         Flags Metric Ref    Use Iface
   default         fritz.box       0.0.0.0         UG    0      0        0 eth0
   172.13.0.0      *               255.255.0.0     U     0      0        0 br-0c5e90369798
   172.17.0.0      *               255.255.0.0     U     0      0        0 docker0
   192.168.1.0     *               255.255.255.0   U     1      0        0 eth0

   # fritz.box -> 192.168.1.2

Delete default route::

   ➜  ip route del default via 192.168.1.2  # untested

Add new default route::

   ➜  ip route add default via 10.1.1.1

Revert to normal::

   ➜  ip route del default via 10.1.1.1
   ➜  ip route add default via 192.168.1.2


