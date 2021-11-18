# prerender-nginx
This is the Prerender.io middleware configuration for an nginx server to allow Google (and other crawlers) to crawl your javascript website.

This file is based on [this](https://gist.github.com/thoop/8165802) and it was updated following the recommendations in the comments

The `nginx.conf` in this repository is full file for __reference__.

Nginx config for
* Single Page Application: [nginx.conf](/nginx.conf)
* PHP application: [nginx-php/nginx.conf](/nginx-php/nginx.conf)
* reverse proxy: [nginx-reverse-proxy/nginx.conf](/nginx-reverse-proxy/nginx.conf)


## debugging

To debug the page sent to prerender.io use the following log format:

```
log_format prerender_debug '[$time_local] $remote_addr - $remote_user - $server_name user-agent: $http_user_agent prerender: $prerender: $request to: $upstream_addr upstream_response_time: $upstream_response_time msec $msec request_time $request_time';
```
