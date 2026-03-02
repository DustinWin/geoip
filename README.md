# 一、 文件说明
## 1. 规则集文件类型
① 重构上游项目 [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip)，生成供下游项目 [DustinWin/ruleset_geodata](https://github.com/DustinWin/ruleset_geodata) 使用的 IP 数据源文件  
② 数据源文件为 [mihomo 内核](https://github.com/MetaCubeX/mihomo) rule-set 规则集文件（.list 格式），包含：`IP-ASN`、`IP-CIDR` 和 `IP-CIDR6` 规则类型，配置 `behavior: classical` 和 `format: text` 后可直接使用  
③ mihomo 内核 geodata 规则集文件，包括：geoip.dat、Country.mmdb、geoip.metadb 和 ASN.mmdb 等  
④ [ShellCrash](https://github.com/juewuy/ShellCrash) 中 CN_IP 绕过内核所需文件，包括：cn_ipv4.txt 和 cn_ipv6.txt，适用于开启“CN_IP 绕过内核”或“CNV6 绕过内核”的使用场景，分别用于替换 *\$CRASHDIR/cn_ip.txt* 和 *\$CRASHDIR/cn_ipv6.txt* 文件；源采用[苍狼山庄/IPNetDB/all_cn.txt](https://ispip.clang.cn/all_cn.txt) 和[苍狼山庄/IPNetDB/all_cn_ipv6.txt](https://ispip.clang.cn/all_cn_ipv6.txt) 组合
## 2. 数据源
① 每天凌晨 2 点（北京时间 UTC+8）自动构建，根据 [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip) 进行深度定制，可点击查看包含的 [IP 段列表](https://github.com/DustinWin/geoip/tree/ips)  
② `geoip,private,🔒 私有网络` & `privateip.list` 源采用 [DustinWin/geoip/config.json](https://github.com/DustinWin/geoip/blob/master/config.json) 中的 `input.type:private`  
③ `geoip,cn,🀄️ 国内 IP` & `cnip.list` & `cn-asn.list` 源采用 [17mon/china_ip_list](https://github.com/17mon/china_ip_list)、[gaoyifan/china-operator-ip](https://github.com/gaoyifan/china-operator-ip) 和 [blackmatrix7/ios_rule_script/ChinaASN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Surge/ChinaASN) 组合  
④ `geoip,telegram,📲 电报消息` & `telegramip.list` & `telegram-asn.list` 源采用 [GeoLite2-ASN-CSV/Telegram](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) 和 [Telegram IP 段](https://core.telegram.org/resources/cidr.txt)组合  
⑤ `geoip,games,🕹️ 游戏平台` & `gamesip.list` 源采用 [blackmatrix7/ios_rule_script/Game](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Game)（仅 IP）  
⑥ `netflixip.list` & `netflix-asn.list` 源采用 [GeoLite2-ASN-CSV/Netflix](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) 和 [blackmatrix7/ios_rule_script/Netflix](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)（Netflix_IP.txt）组合  
⑦ `geoip,media,🌍 国外媒体` & `mediaip.list` 源采用 [blackmatrix7/ios_rule_script/GlobalMedia](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/GlobalMedia)（仅 IP）
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
    <td rowspan="3" align="center"><a href="https://github.com/Loyalsoldier/geoip/tree/release/text">点此查看</a></td>
    <td><a href="https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/geoip-all.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/geoip-all.dat">点此下载</a></td>
    <td><a href="https://ghfast.top/https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/geoip-all.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-all.mmdb</td>
    <td><a href="https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/Country-all.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/Country-all.mmdb">点此下载</a></td>
    <td><a href="https://ghfast.top/https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/Country-all.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-all.metadb</td>
    <td><a href="https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/geoip-all.metadb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/geoip-all.metadb">点此下载</a></td>
    <td><a href="https://ghfast.top/https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/geoip-all.metadb">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-ASN-all.mmdb</td>
    <td><code>cloudflare</code></del>、<code>cloudfront</code>、<code>facebook</code>、<code>fastly</code>、<code>google</code>、<code>netflix</code>、<code>telegram</code> 和 <code>twitter</code>，具体可<a href="https://github.com/Loyalsoldier/geoip/blob/master/asn.csv">点此查看</a></td>
    <td><a href="https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/Country-ASN-all.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/Country-ASN-all.mmdb">点此下载</a></td>
    <td><a href="https://ghfast.top/https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/Country-ASN-all.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip.dat</td>
    <td rowspan="3"><code>private</code>、<code>cn</code>、<code>telegram</code>、<code>games</code> 和 <code>media</code></td>
    <td><a href="https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/geoip.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/geoip.dat">点此下载</a></td>
    <td><a href="https://ghfast.top/https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/geoip.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>Country.mmdb</td>
    <td><a href="https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/Country.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/Country.mmdb">点此下载</a></td>
    <td><a href="https://ghfast.top/https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/Country.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip.metadb</td>
    <td><a href="https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/geoip.metadb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/geoip.metadb">点此下载</a></td>
    <td><a href="https://ghfast.top/https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/geoip.metadb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-lite.dat</td>
    <td rowspan="3"><code>private</code>、<code>cn</code>、<code>telegram</code>、<del><code>games</code></del> 和 <del><code>media</code></del></td>
    <td><a href="https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/geoip-lite.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/geoip-lite.dat">点此下载</a></td>
    <td><a href="https://ghfast.top/https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/geoip-lite.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-lite.mmdb</td>
    <td><a href="https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/Country-lite.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/Country-lite.mmdb">点此下载</a></td>
    <td><a href="https://ghfast.top/https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/Country-lite.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-lite.metadb</td>
    <td><a href="https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/geoip-lite.metadb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/geoip-lite.metadb">点此下载</a></td>
    <td><a href="https://ghfast.top/https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/geoip-lite.metadb">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-ASN.mmdb</td>
    <td><code>telegram</code> 和 <code>netflix</code>，具体可<a href="https://github.com/DustinWin/geoip/blob/master/asn.csv">点此查看</a></td>
    <td><a href="https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/Country-ASN.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/Country-ASN.mmdb">点此下载</a></td>
    <td><a href="https://ghfast.top/https://github.com/DustinWin/geoip/releases/download/mihomo-geodata/Country-ASN.mmdb">点此下载</a></td>
  </tr>
</table>

# 三、 文件导入
## 1. 导入 Linux 端（以 ShellCrash 导入 geoip.dat、Country.mmdb、geoip.metadb 和 ASN.mmdb 为例）
连接 SSH 后执行如下命令：
```shell
curl -o $CRASHDIR/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/geoip.dat
curl -o $CRASHDIR/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/Country.mmdb
curl -o $CRASHDIR/geoip.metadb -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/geoip.metadb
curl -o $CRASHDIR/ASN.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/Country-ASN.mmdb
$CRASHDIR/start.sh restart
```
## 2. 导入 Windows 端（以 [Clash Verge](https://github.com/clash-verge-rev/clash-verge-rev) 导入 geoip.dat、Country.mmdb、geoip.metadb 和 ASN.mmdb 为例）
以管理员身份运行 CMD，执行如下命令：
```shell
taskkill /f /t /im "Clash Verge*"
taskkill /f /t /im Clash-Verge*
taskkill /f /t /im clash-meta*
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\geoip.dat -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/geoip.dat
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/Country.mmdb
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\geoip.metadb -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/geoip.metadb
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\ASN.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/geoip@mihomo-geodata/Country-ASN.mmdb
pause
```
