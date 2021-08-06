不会git ，懒得整。直接打包了。

这个包 ngx_lua_module 是基于 lua-nginx-module-0.10.14 版本。不基于依赖luaJIT。

主要增加 capture_multi 函数，可以对不同子请求指定不同header

其他用法一样。

例如：
header_info = {}
header_info["User-xxxx"]="xxxx-ddd-ccccc";

table.insert(uri_list, {v.url,{ method = ngx.HTTP_POST,args = query,body=body,header=header_info} })

ngx_lua_module 10.14.2 增加了
sha256 bin2hex hex2bin hmac_sha256
