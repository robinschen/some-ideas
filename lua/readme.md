#!/bin/bash

# 设置要封禁的 IP 地址
IP="192.168.1.1"

# 发起 POST 请求设置 IP 到 Lua Shared Dict
curl -X POST http://your_server/setBlockIp -d "ip=$IP"

### save ip list to /usr/local/openresty/data/blockip_dict.txt

### test localhost
<!--  -->
curl -v http://localhost/ 

### you can dynamic add block ip
curl -X POST http://localhost/setBlockIp -d "ip=127.0.0.1"

### test result
curl -v http://localhost/ 