nginx-rtmp-win64
================

* Nginx: 1.19.6
* Nginx-Rtmp-Module: 1.2.1
* Nginx-Rtmpt-Proxy-Module: commit 5f3bb0c
* openssl-1.1.1i
* pcre-8.44
* zlib-1.2.11

# configure arguments
```
nginx version: nginx/1.19.5
built by cl 19.27.29111 for x64

TLS SNI support enabled
configure arguments:
--with-cc=cl \
--builddir=objs \
--with-debug \
--prefix= \
--conf-path=conf/nginx.conf \
--pid-path=logs/nginx.pid \
--http-log-path=logs/access.log \
--error-log-path=logs/error.log \
--sbin-path=nginx.exe \
--http-client-body-temp-path=temp/client_body_temp \
--http-proxy-temp-path=temp/proxy_temp \
--http-fastcgi-temp-path=temp/fastcgi_temp \
--http-scgi-temp-path=temp/scgi_temp \
--http-uwsgi-temp-path=temp/uwsgi_temp \
--with-cc-opt=-DFD_SETSIZE=1024 \
--with-select_module \
--with-http_v2_module \
--with-http_realip_module \
--with-http_addition_module \
--with-http_sub_module \
--with-http_dav_module \
--with-http_stub_status_module \
--with-http_flv_module \
--with-http_mp4_module \
--with-http_gunzip_module \
--with-http_gzip_static_module \
--with-http_auth_request_module \
--with-http_random_index_module \
--with-http_secure_link_module \
--with-http_slice_module \
--with-mail \
--with-stream \
--with-http_ssl_module \
--with-mail_ssl_module \
--with-stream_ssl_module \
--with-openssl=objs/lib/openssl-1.1.1i --with-openssl-opt=no-asm \
--with-pcre=objs/lib/pcre-8.44 \
--with-zlib=objs/lib/zlib-1.2.11 \
--add-module=objs/lib/nginx-rtmp-module \
--add-module=objs/lib/nginx-rtmpt-proxy-module
```

# Instructions
Double-click nginx_x64.exe

# A brief description
conf/nginx.conf is an example of configuration file
RTMP monitors port 1935, and enables live applications
HTTP listens on port 8080,
* :8080/stat View stream status
* :8080/play.html is a live hls tester (fixed address for localhost with streamkey "boo" -> http://localhost/hls/boo/)

RTMP live stream: rtmp://<ip>/live/streamkey
HLS stream: http://<ip>/hls/streamkey/
DASH stream: http://<ip>/dash/streamkey/
