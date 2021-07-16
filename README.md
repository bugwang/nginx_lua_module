# nginx_lua_module 是基于 lua-nginx-module-0.10.14 版本。没有luajit

增加 capture_multi 的 不同请求的 可以指定不同header

其他用法一样。
例如：
header_info = {}
header_info["User-xxxx"]="xxxx/post";

table.insert(uri_list, {v.url,{ method = ngx.HTTP_POST,args = query,body=body,header=header_info} })


