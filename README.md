# -X-
改自Lucy
# 基于[＠KOP-XIAO](https://github.com/KOP-XIAO/QuantumultX/blob/master/QuantumultX_Profiles.conf)修改
# Author:https://github.com/Repcz
# TG:https://t.me/QVQ_Channel
#
# 以 ';' 或 '#' 或 '//' 开头的配置文件行为注释行
#
# 最后更新时间: 2024-07-27 22:50
#
# ================

[general]
# 节点延迟测试链接
server_check_url = http://latency-test.skk.moe/endpoint
# 网络连通性测试链接
network_check_url = http://connectivitycheck.platform.hicloud.com/generate_204
# 测试超时时间 (毫秒)
server_check_timeout = 3000
# 关联配置图标
profile_img_url = https://avatars.githubusercontent.com/repcz
# 节点页面的节点信息展示，可完整自定义展示内容与方式
geo_location_checker = disabled
;geo_location_checker = http://ip-api.com/json/?lang=zh-CN, https://raw.githubusercontent.com/ConnersHua/RuleGo/master/Quantumult/Script/geo_location_checker.js
# 资源解析器，可用于自定义各类远程资源的转换，如节点，规则 filter，复写 rewrite 等，url 地址可远程，可 本地/iCloud(Quantumult X/Scripts目录);
resource_parser_url = https://git.988896.xyz/https://raw.githubusercontent.com/KOP-XIAO/QuantumultX/master/Scripts/resource-parser.js
# 下列路径将不经过QuanX的处理,设置后建议重启设备
excluded_routes = 239.255.255.250/32
# UDP　Drop名单
udp_drop_list = 443
# 第一个filter为4g模式开启规则分流，第二个filter为其他wifi下开启规则分流，第三个wifi1修改成你路由器翻墙的wifi名开启直连模式，第四个wifi2为你公司或者其他有路由器翻墙的WiFi名走直连）
# 默认关闭根据wifi切换模式，如需开启，删除下方的";"即可
; running_mode_trigger = filter, filter, filter:all_direct, filter: all_direct
# dns exclusion list中的域名将不使用fake-ip方式. 其它域名则全部采用 fake-ip 及远程解析的模式
dns_exclusion_list = *.lan, *.direct, cable.auth.com, *.msftconnecttest.com, *.msftncsi.com, network-test.debian.org, detectportal.firefox.com, resolver1.opendns.com, *.srv.nintendo.net, *.stun.playstation.net, xbox.*.microsoft.com, *.xboxlive.com, stun.*, global.turn.twilio.com, global.stun.twilio.com, app.yinxiang.com, injections.adguard.org, local.adguard.org, cable.auth.com, localhost.*.qq.com, localhost.*.weixin.qq.com, *.logon.battlenet.com.cn, *.logon.battle.net, *.blzstatic.cn, music.163.com, *.music.163.com, *.126.net, musicapi.taihe.com, music.taihe.com, songsearch.kugou.com, trackercdn.kugou.com, *.kuwo.cn, api-jooxtt.sanook.com, api.joox.com, joox.com, y.qq.com, *.y.qq.com, streamoc.music.tc.qq.com, mobileoc.music.tc.qq.com, isure.stream.qqmusic.qq.com, dl.stream.qqmusic.qq.com, aqqmusic.tc.qq.com, amobile.music.tc.qq.com, *.xiami.com, *.music.migu.cn, music.migu.cn, proxy.golang.org, *.mcdn.bilivideo.cn, *.cmpassport.com, id6.me, open.e.189.cn, mdn.open.wo.cn, opencloud.wostore.cn, auth.wosms.cn, *.jegotrip.com.cn, *.icitymobile.mobi, *.pingan.com.cn, *.cmbchina.com, *.10099.com.cn, pool.ntp.org, *.pool.ntp.org, ntp.*.com, time.*.com, ntp?.*.com, time?.*.com, time.*.gov, time.*.edu.cn, *.ntp.org.cn, PDC._msDCS.*.*, DC._msDCS.*.*, GC._msDCS.*.*
# 节点不支持UDP转发时返回的策略：direct/reject/节点
fallback_udp_policy = reject

[dns]

# 禁用系统 DNS
no-system
# 禁用 IPv6
no-ipv6

# DNS服务器 支持参数 excluded_ssids , included_ssids指定在特定 Wi-Fi下失效/生效
server = 223.5.5.5
server = 119.29.29.29

# 使用 DoH3，DNS over HTTP/3，须开启下面参数
;prefer-doh3
# 指定 doh 服务，则上面的一般 dns 解析均失效
;doh-server = https://120.53.53.53/dns-query, https://223.5.5.5/dns-query
# 如指定了 DoQ 服务，则 DoH 以及其它 dns解析均失效
;doq-server quic://223.5.5.5, quic://223.6.6.6

[policy]

static=手动切换, 香港节点, 美国节点, 狮城节点, 日本节点, 台湾节点, direct, server-tag-regex=., img-url=https://raw.githubusercontent.com/fmz200/wool_scripts/main/icons/chxm1023/Quantumult_X_1.png
static=国外网站, 手动切换, 香港节点, 美国节点, 狮城节点, 日本节点, 台湾节点, proxy, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Global.png
static=国际媒体, 手动切换, 香港节点, 美国节点, 狮城节点, 日本节点, 台湾节点, proxy, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/YouTube.png
static=微软服务, 手动切换, 香港节点, 美国节点, 狮城节点, 日本节点, 台湾节点, proxy, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Microsoft.png
static=谷歌服务, 手动切换, 香港节点, 美国节点, 狮城节点, 日本节点, 台湾节点, proxy, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Google_Search.png
static=电报消息, 手动切换, 香港节点, 美国节点, 狮城节点, 日本节点, 台湾节点, proxy, direct, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Telegram.png
static=推特消息, 手动切换, 香港节点, 美国节点, 狮城节点, 日本节点, 台湾节点, proxy, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Twitter.png
static=AI, 手动切换, 香港节点, 美国节点, 狮城节点, 日本节点, 台湾节点, proxy, img-url=https://raw.githubusercontent.com/Orz-3/mini/master/Color/OpenAI.png
static=游戏平台, 手动切换, 香港节点, 美国节点, 狮城节点, 日本节点, 台湾节点, proxy, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Game.png
static=Spotify, 手动切换, 香港节点, 美国节点, 狮城节点, 日本节点, 台湾节点, proxy, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Spotify.png
static=Emby, 手动切换, 香港节点, 美国节点, 狮城节点, 日本节点, 台湾节点, direct, server-tag-regex=., img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Emby.png
static=兜底分流, 手动切换, 香港节点, 美国节点, 狮城节点, 日本节点, 台湾节点, direct, proxy, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Final.png

url-latency-benchmark=香港节点, server-tag-regex=(?i)🇭🇰|香港|(\b(HK|Hong)\b), check-interval=300, alive-checking=false, tolerance=0, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Hong_Kong.png
url-latency-benchmark=美国节点, server-tag-regex=(?i)🇺🇸|美国|洛杉矶|圣何塞|(\b(US|United States)\b), check-interval=300, alive-checking=false, tolerance=0, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/United_States.png
url-latency-benchmark=狮城节点, server-tag-regex=(?i)🇸🇬|新加坡|狮|(\b(SG|Singapore)\b), check-interval=300, alive-checking=false, tolerance=0, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Singapore.png
url-latency-benchmark=日本节点, server-tag-regex=(?i)🇯🇵|日本|东京|(\b(JP|Japan)\b), check-interval=300, alive-checking=false, tolerance=0, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Japan.png
url-latency-benchmark=台湾节点, server-tag-regex=(?i)🇨🇳|🇹🇼|台湾|(\b(TW|Tai|Taiwan)\b), check-interval=300, alive-checking=false, tolerance=0, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/China.png

[server_local]


[server_remote]
https://fbapiv2.fbsublink.com/flydsubal/xreolah5jv8hrvwg?clash=1&extend=1&overseas=1, tag=飞鸟, update-interval=172800, opt-parser=true, enabled=false


[filter_remote]

https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/Reject.list, tag=Reject, force-policy=reject, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/DDCX.snippet, tag=AD_DiDiChuXing, force-policy=reject, update-interval=172800, opt-parser=false, inserted-resource=true, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/AI.list, tag=AI, force-policy=AI, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/YouTube.list, tag=Youtube, force-policy=谷歌服务, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/Google.list, tag=Google, force-policy=谷歌服务, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/Github.list, tag=Github, force-policy=微软服务, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/Microsoft.list, tag=Microsoft, force-policy=微软服务, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/OneDrive.list, tag=OneDrive, force-policy=微软服务, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/Epic.list, tag=Epic, force-policy=游戏平台, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/Twitter.list, tag=Twitter, force-policy=推特消息, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/Telegram.list, tag=Telegram, force-policy=电报消息, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/Emby.list, tag=Emby, force-policy=Emby, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/Spotify.list, tag=Spotify, force-policy=Spotify, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/Bahamut.list, tag=Bahamut, force-policy=国际媒体, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/Netflix.list, tag=Netflix, force-policy=国际媒体, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/PrimeVideo.list, tag=PrimeVideo, force-policy=国际媒体, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/HBO.list, tag=HBO, force-policy=国际媒体, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/TikTok.list, tag=TikTok, force-policy=国际媒体, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/ProxyGFW.list, tag=ProxyGFW, force-policy=国外网站, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/AppleProxy.list, tag=AppleProxy, force-policy=国外网站, update-interval=172800, opt-parser=false, enabled=true
https://github.com/Repcz/Tool/raw/X/QuantumultX/Rules/Apple.list, tag=Apple, force-policy=DIRECT, update-interval=172800, opt-parser=false, enabled=true
FILTER_LAN, tag=LAN, force-policy=direct, enabled=true
FILTER_REGION, tag=CN, force-policy=direct, enabled=true

[filter_local]

final, 兜底分流

[rewrite_local]


[rewrite_remote]
https://raw.githubusercontent.com/chxm1023/Advertising/main/AppAd.conf, tag=App广告拦截, update-interval=172800, opt-parser=true, enabled=true
https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/WebPage.conf, tag=网页去广告@RuCu6, update-interval=172800, opt-parser=false, enabled=true
https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/MyBlockAds.conf, tag=MyBlockAds@RuCu6, update-interval=172800, opt-parser=false,  enabled=true
https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/Cube/zhihu.snippet, tag=知乎去广告@RuCu6, update-interval=172800, opt-parser=false, enabled=true
https://raw.githubusercontent.com/Keywos/rule/main/script/weibo_us/wb_us.sgmodule, tag=微博国际版去广告@keywos@kokoryh, update-interval=172800, opt-parser=true, enabled=true
https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/Cube/weibo.snippet, tag=微博去广告@RuCu6, update-interval=172800, opt-parser=false, enabled=true
https://raw.githubusercontent.com/ZenmoFeiShi/Qx/main/Smzdm.snippet, tag=什么值得买去广告@ZenmoFeiShi, update-interval=172800, opt-parser=false,  enabled=true
https://raw.githubusercontent.com/fmz200/wool_scripts/main/QuantumultX/rewrite/cleanup.snippet, tag=App&小程序净化合集@fmz200, update-interval=172800, opt-parser=false, enabled=true
https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/Cube/youtube.snippet, tag=YouTube去广告@RuCu6, update-interval=86400, opt-parser=false, enabled=true
https://raw.githubusercontent.com/ddgksf2013/Rewrite/master/Function/Bilibili_CC.conf, tag=B站繁体翻译@ddkgsf2013, update-interval=172800, opt-parser=false, enabled=true
https://raw.githubusercontent.com/DualSubs/YouTube/main/modules/DualSubs.YouTube.snippet, tag=油管双语@DualSubs , update-interval=172800, opt-parser=false, enabled=true
https://raw.githubusercontent.com/DualSubs/Spotify/main/modules/DualSubs.Spotify.snippet, tag=Spotify双语@DualSubs, update-interval=172800, opt-parser=false, enabled=true
https://raw.githubusercontent.com/app2smile/rules/master/module/spotify.conf, tag=Spotify解锁@app2smile, update-interval=172800, opt-parser=true, enabled=true
https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/TestFlightDownload.conf, tag=TF下载解锁@NobyDa, update-interval=172800, opt-parser=false, enabled=true
https://raw.githubusercontent.com/Peng-YM/Sub-Store/master/config/QX.snippet, tag=Sub-Store, update-interval=172800, opt-parser=false, enabled=true
https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.quanx.conf, tag=BoxJS@chavyleung, update-interval=172800, opt-parser=false, enabled=true

[task_local]
0 0 0,1,2,20,21,22,23 * * ? https://raw.githubusercontent.com/xiaomaoJT/QxScript/main/rewrite/boxJS/XiaoMaoSCV.js, tag=🚗XiaoMao学习车, img-url=https://raw.githubusercontent.com/LovedGM/Quantumult-X-TuBiao/main/zishi-cs/zs3.png, enabled=false
0 0 9 * * ? https://raw.githubusercontent.com/xiaomaoJT/QxScript/main/rewrite/boxJS/XiaoMaoTyhoon.js, tag=🌀XiaoMao_台风监测, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Blackhole.png, enabled=true
0 0 22 * * ? https://raw.githubusercontent.com/xiaomaoJT/QxScript/main/rewrite/boxJS/XiaoMaoImprisonNovel.js, tag=🔞XiaoMao_大师文学, img-url=graduationcap.fill.system, enabled=false
event-interaction https://raw.githubusercontent.com/getsomecat/Qx/main/Net_Speed.js, tag=⚡️ Net Speed, img-url=bolt.square.fill.system, enabled=true

event-interaction https://raw.githubusercontent.com/xream/scripts/main/surge/modules/network-info/net-lsp-x.js, tag=网络信息 𝕏, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Global.png, enabled=true
event-interaction https://raw.githubusercontent.com/KOP-XIAO/QuantumultX/master/Scripts/streaming-ui-check.js, tag=流媒体解锁查询, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Color/Siri.png, enabled=true

# 手动添加
; https://raw.githubusercontent.com/KOP-XIAO/QuantumultX/master/Scripts/UI-Action.json

[http_backend]


[mitm]
passphrase = 62E78025
p12 = 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

# 跳过验证证书
skip_validating_cert = false
# 强制嗅探域名
force_sni_domain_name = false
# 主机名
hostname = -weather-data.apple.com

# 当使用 Quantumult X 在 M 芯片的 Mac 设备上作为局域网网关时，使用下面的参数来 跳过某些特定设备的 mitm 需求
;skip_src_ip = 192.168.4.0, 92.168.4.51
# 当多个不同的 TCP 连接（非域名类请求）的目标 IP 不同，但这些连接的 TSL 握手 SNI 字段相同时，如需跳过其中某些连接的 MitM hostname 匹配过程，可使用👇参数。
;skip_dst_ip = 123.44.55.4
