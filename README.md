# 一、 文件说明
## 1. 规则集文件类型
① [Clash](https://github.com/Dreamacro/clash) geodata 规则集文件，包括：geoip.dat、Country.mmdb 和 geoip.metadb、ASN.mmdb（仅限 [mihomo 内核](https://github.com/MetaCubeX/mihomo)）等  
② Clash rule-set 规则集文件（.list 格式），适用于 `behavior: classical` 且 `format: text` 的使用场景，包含 `IP-ASN`、`IP-CIDR` 和 `IP-CIDR6` 规则类型  
③ [sing-box](https://github.com/SagerNet/sing-box) geodata 规则集文件，包括：geoip.db 等
## 2. 数据源
① 每天凌晨 2 点（北京时间）自动构建，根据 [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip) 进行深度定制，可点击查看包含的 [IP 段列表](https://github.com/DustinWin/geoip/tree/ips)  
② `geoip,netflix,🎥 奈飞视频` & `netflixip.list` 源采用 [GeoLite2/netflix.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) 和 [blackmatrix7/ios_rule_script/Netflix](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)（仅 IP）组合  
③ `geoip,telegram,📲 电报消息` & `telegramip.list` 源采用 [GeoLite2/telegram.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[Telegram IP 段](https://core.telegram.org/resources/cidr.txt) 和 [blackmatrix7/ios_rule_script/Telegram](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Telegram)（仅 IP）组合  
④ `geoip,private,🔒 私有网络` & `privateip.list` 源采用 [GeoLite2/private.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（仅 IP）和 [TrackersList](https://github.com/XIU2/TrackersListCollection/blob/master/all.txt)（仅 IP）组合  
⑤ `geoip,cn,🇨🇳 直连 IP` & `cnip.list` 源采用 [GeoLite2/cn.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[17mon/china_ip_list](https://github.com/17mon/china_ip_list)、[gaoyifan/china-operator-ip](https://github.com/gaoyifan/china-operator-ip)、[blackmatrix7/ios_rule_script/ChinaIPs](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaIPs) 和 [APNIC/CN](https://ftp.apnic.net/stats/apnic/delegated-apnic-latest) 组合
# 二、 文件下载
**规则集文件包含的规则和下载地址对应关系如下表：**
<table>
  <tr>
    <td><b>规则集文件名称</b></td>
    <td align="center"><b>包含规则</b></td>
    <td><b>GitHub 源</b></td>
    <td><b>jsDelivr 源</b></td>
    <td><b>GitHub Proxy 源</b></td>
  </tr>
  <tr>
    <td>geoip-all.dat</td>
    <td rowspan="4" align="center"><a href="https://github.com/Loyalsoldier/geoip/tree/release/text">点此查看</a></td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/clash/geoip-all.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/geoip-all.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/clash/geoip-all.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-all.mmdb</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/clash/Country-all.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/Country-all.mmdb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/clash/Country-all.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-all.metadb</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/clash/geoip-all.metadb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/geoip-all.metadb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/clash/geoip-all.metadb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-all.db</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/sing-box/geoip-all.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@sing-box/geoip-all.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/sing-box/geoip-all.db">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-ASN-all.mmdb</td>
    <td><code>cloudflare</code></del>、<code>cloudfront</code>、<code>facebook</code>、<code>fastly</code>、<code>google</code>、<code>netflix</code>、<code>telegram</code> 和 <code>twitter</code>，具体可<a href="https://github.com/Loyalsoldier/geoip/blob/master/asn.csv">点此查看</a></td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/clash/Country-ASN-all.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/Country-ASN-all.mmdb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/clash/Country-ASN-all.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip.dat</td>
    <td rowspan="4"><code>netflix</code>、<code>telegram</code>、<code>private</code> 和 <code>cn</code></td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/clash/geoip.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/geoip.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/clash/geoip.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>Country.mmdb</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/clash/Country.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/Country.mmdb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/clash/Country.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip.metadb</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/clash/geoip.metadb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/geoip.metadb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/clash/geoip.metadb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip.db</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/sing-box/geoip.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@sing-box/geoip.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/sing-box/geoip.db">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-lite.dat</td>
    <td rowspan="4"><del><code>netflix</code></del>、<code>telegram</code>、<code>private</code> 和 <code>cn</code></td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/clash/geoip-lite.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/geoip-lite.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/clash/geoip-lite.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-lite.mmdb</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/clash/Country-lite.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/Country-lite.mmdb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/clash/Country-lite.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-lite.metadb</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/clash/geoip-lite.metadb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/geoip-lite.metadb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/clash/geoip-lite.metadb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-lite.db</td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/sing-box/geoip-lite.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@sing-box/geoip-lite.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/sing-box/geoip-lite.db">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-ASN.mmdb</td>
    <td><code>netflix</code>、<code>telegram</code>、<del><code>private</code> 和 <code>cn</code></del>，具体可<a href="https://github.com/DustinWin/geoip/blob/master/asn.csv">点此查看</a></td>
    <td><a href="https://raw.githubusercontent.com/DustinWin/geoip/clash/Country-ASN.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/Country-ASN.mmdb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://raw.githubusercontent.com/DustinWin/geoip/clash/Country-ASN.mmdb">点此下载</a></td>
  </tr>
</table>

# 三、 文件导入
① 导入 Linux 端（以 [ShellCrash](https://github.com/juewuy/ShellCrash) 导入 geoip.dat、Country.mmdb、geoip.metadb、ASN.mmdb 和 geoip.db 为例）  
连接 SSH 后执行如下命令：
```
# Clash 内核
curl -o $CRASHDIR/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/geoip.dat
curl -o $CRASHDIR/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/Country.mmdb
# mihomo 内核
curl -o $CRASHDIR/geoip.metadb -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/geoip.metadb
curl -o $CRASHDIR/ASN.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/Country-ASN.mmdb
# sing-box 内核
curl -o $CRASHDIR/geoip.db -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@sing-box/geoip.db
$CRASHDIR/start.sh restart
```
② 导入 Windows 端（以 [Clash Verge](https://github.com/clash-verge-rev/clash-verge-rev) 导入 geoip.dat、Country.mmdb、geoip.metadb 和 ASN.mmdb 为例）  
以管理员身份运行 CMD，执行如下命令：
```
taskkill /f /t /im "Clash Verge*"
taskkill /f /t /im Clash-Verge*
taskkill /f /t /im clash-meta*
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\geoip.dat -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/geoip.dat
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/Country.mmdb
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\geoip.metadb -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/geoip.metadb
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\ASN.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@clash/Country-ASN.mmdb
pause
```
