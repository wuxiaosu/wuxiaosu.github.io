---
title: "几个 ip 信息获取接口"
date: 2022-05-24T22:06:48+08:00
draft: true
---
+ <http://ipinfo.io/json>  

```json
{
  "ip": "59.42.111.132",
  "hostname": "132.111.42.59.broad.gz.gd.dynamic.163data.com.cn",
  "city": "Lianjiang",
  "region": "Guangdong",
  "country": "CN",
  "loc": "21.6467,110.2817",
  "org": "AS4134 CHINANET-BACKBONE",
  "timezone": "Asia/Urumqi",
  "readme": "https://ipinfo.io/missingauth"
}
```

+ <http://whois.pconline.com.cn/ip.jsp>  

```bash
广东省广州市天河区 电信ADSL
```

+ <http://pv.sohu.com/cityjson?ie=utf-8>  

```bash
var returnCitySN = {"cip": "59.42.111.132", "cid": "440106", "cname": "广东省广州市天河区"};
```  
