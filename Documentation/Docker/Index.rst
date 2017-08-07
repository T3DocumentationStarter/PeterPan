.. include:: ../Includes.txt

======
Docker
======

Ubuntu, Docker, Remote API
==========================


-  https://www.google.de/search?q=ubuntu+Docker+Remote+API
-  `Ubuntu 14.04: Quick Tip – How to enable Docker Remote API?
   <http://www.virtuallyghetto.com/2014/07/quick-tip-how-to-enable-docker-remote-api.html>`__
-  `Ubuntu 16.04: Enabling Docker Remote API
   <https://www.ivankrizsan.se/2016/05/18/enabling-docker-remote-api-on-ubuntu-16-04/>`__
   
   
Nginx reverse-proxy
===================
Keywords: Automated Nginx Reverse Proxy for Docker

Background:

-  `Why Use A Reverse Proxy With Docker? 
   <http://jasonwilder.com/blog/2014/03/25/automated-nginx-reverse-proxy-for-docker/>`__

Readings:

-  https://github.com/jwilder/nginx-proxy/blob/master/README.md
-  ct.17.15.110-115-Docker-Container-für-Heim-und-Webserver

:file:`/etc/apache2/sites-enabled/docker-local-proxy.conf`::

   <VirtualHost *:80>
      ServerName proxy.docker.local:80
      ServerAlias abc.docker.local bcd.docker.local devdocs.docker.local
       # ProxyRequests Off
       # ProxyVia Off
       <Proxy *>
            Require all granted
       </Proxy>
      ProxyPreserveHost On
       ProxyPass        / http://127.0.0.1:3880/
       ProxyPassReverse / http://127.0.0.1:3880/ 
   </VirtualHost>

   # vim: syntax=apache ts=4 sw=4 sts=4 sr noet
   # https://confluence.atlassian.com/kb/proxying-atlassian-server-applications-with-apache-http-server-mod_proxy_http-806032611.html
   
:file:`/etc/hosts`::

   127.0.0.1       abc.docker.local
   127.0.0.1       bcd.docker.local
   127.0.0.1       devdocs.docker.local
   127.0.0.1       phpmyadmin.docker.local
   127.0.0.1       proxy.docker.local

Examples::

   run -d --rm -e VIRTUAL_HOST=abc.docker.local nginx
   run -d --rm -e VIRTUAL_HOST=bcd.docker.local nginx
   

