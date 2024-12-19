# ===============================

# Quantumult X 配置文件

# ===============================

[general]

# 通用配置，例如 DNS、流量统计等

# > 用于节点延迟测试

server_check_url = http://www.gstatic.com/generate_204

# > 服务器测试超时时间 (毫秒)

server_check_timeout = 3000

# > 用于设置图标显示

profile_img_url = https://github.githubassets.com/images/modules/site/integrators/google.png

# > 用于 Check 节点 IP 地址

geo_location_checker = http://ip-api.com/json/?lang=zh-CN, https://raw.githubusercontent.com/KOP-XIAO/QuantumultX/master/Scripts/IP_API.js

# > 功能强大的解析器，用于引用资源的转换

resource_parser_url = https://raw.githubusercontent.com/KOP-XIAO/QuantumultX/master/Scripts/resource-parser.js

# > 下列路径将不经过 QuanX 的处理

excluded_routes = 239.255.255.250/32, 24.105.30.129/32, 185.60.112.157/32, 185.60.112.158/32, 182.162.132.1/32

udp*whitelist = 1-442, 444-65535
dns_exclusion_list = *.10099.com.cn, _.cmpassport.com, _.jegotrip.com.cn, \_.icitymobile.mobi, id6.me, \*.pingan.com.cn

# ===============================

# GeoLite2 「其他设置」里「GeoLite2」的「来源」填写使用下面链接「任选一个」，并开启「自动更新」

# ===============================

# https://raw.githubusercontent.com/Loyalsoldier/geoip/release/Country.mmdb

# https://github.com/Hackl0us/GeoIP2-CN/raw/release/Country.mmdb

# ===============================

# 节点服务器部分

# ===============================

[server_local]

# 本地代理服务器

[server_remote]

# 远程代理服务器（SSR、V2Ray、Trojan、Socks 等）

# ===============================

# 策略组部分

# ===============================

[policy]

# 定义策略组和故障转移、自动选择等

# ===============================

# 远程分流规则

# ===============================

[filter_remote]

# ===============================

# 本地分流规则

# ===============================

[filter_local]

# 本地定义的分流规则

final, direct
geoip, cn, direct
host-suffix, local, direct

# ===============================

# 重写部分

# ===============================

[rewrite_local]

# 本地定义的重写规则

# REWRITE, HEADER 规则

# ===============================

# 远程重写部分

# ===============================

[rewrite_remote]

# 从远程获取的重写规则

# ===============================

# DNS 部分

# ===============================

[dns]

# DNS 配置

no-ipv6
no-system
server = 223.5.5.5
server = 119.29.29.29
server = 114.114.114.114
server = /_.icloud.com/119.29.29.29
server = /_.icloud.com.cn/119.29.29.29
server = /_.tencent.com/119.29.29.29
server = /_.weixin.com/119.29.29.29

# ===============================

# 定时任务部分

# ===============================

[task_local]

# 定义定时任务，例如定期测速、数据同步等

# ===============================

# HTTP Backend 部分

# ===============================

[http_backend]

# ===============================

# MITM 配置部分

# ===============================

[mitm]
passphrase = 6FF196F6
p12 =
skip_validating_cert = true
force_sni_domain_name = false
hostname = -*.apple.com, -consumer.fcbox.com, -*huami.com, -weather-data.apple.com, -*amemv.com, -*snssdk.com, -www.google.com
