下载nginx 改名放到/usr/local/nginx/   
在其内
./configure 
 --with-select_module
 --with-poll_module 
 --with-threads
 --with-file-aio
 --with-http_ssl_module
--with-http_realip_module
--with-http_v2_module
--with-http_mp4_module

./configure
    --sbin-path=/usr/local/nginx/nginx
    --conf-path=/usr/local/nginx/nginx.conf
    --pid-path=/usr/local/nginx/nginx.pid
    --with-http_ssl_module
    --with-pcre=../pcre-8.44
    --with-zlib=../zlib-1.2.11
    --with-http_gzip_static_module
    
    
Building nginx from Sources by configure command in linux
http://nginx.org/en/docs/configure.html

--prefix=path
/usr/local/nginx directory by default
--sbin-path=path 
prefix/sbin/nginx
--modules-path 
prefix/logs/error.log
prefix/logs/nginx.pid

--with-select_module
--with-poll_module 
--with-threads
--with-file-aio

--with-http_ssl_module
enables building a module that adds the HTTPS protocol support to an HTTP server. This module is not built by default. The OpenSSL library is required to build and run this module.


--with-http_realip_module
启用HTTP_Realip模块，用于修改客户端请求头中客户端IP地址值，一般用于反向代理中，将真实的客户端IP传送给后端的应用服务器。默认情况下不构建此模块。

--with-http_v2_module

--with-http_flv_module
--with-http_mp4_module
启用HTTP_FLV模块，用于为Flash Video（FLV）文件提供伪流视频服务端支持，开启它则允许在网页上播放FLV格式的视频。默认情况下不构建此模块。
启用HTTP_MP4模块，用于为MP4格式的视频文件提供伪流视频服务端支持，开启它则允许在网页上播放MP4格式的视频。默认情况下不构建此模块。
--with-http_mp4_module
enables building the ngx_http_mp4_module module that provides pseudo-streaming server-side support for MP4 files. This module is not built by default.
--with-http_gunzip_module
enables building the ngx_http_gunzip_module module that decompresses responses with “Content-Encoding: gzip” for clients that do not support “gzip” encoding method. This module is not built by default.
--with-http_gzip_static_module
enables building the ngx_http_gzip_static_module module that enables sending precompressed files with the “.gz” filename extension instead of regular files. This module is not built by default.
