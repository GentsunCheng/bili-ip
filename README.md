# Clash rule-provider
clash provider由先后顺序依次排序，已经出现的规则在后面直接抛弃，请确保你的自定义规则在最前面

通过如下方法加入你的规则

``` yaml
rule-providers:
  google-vpn:
    type: http
    behavior: ipcidr
    url: "https://cdn.jsdelivr.net/gh/GentsunCheng/provider/google-vpn.txt"
    path: ./ruleset/google-vpn.yaml
    interval: 86400 
  bili-ip:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/GentsunCheng/provider/bili-ip.txt"
    path: ./ruleset/bili-ip.yaml
    interval: 86400
 ```
