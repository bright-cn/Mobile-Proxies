# Bright Data 移动代理

[![Promo](https://github.com/bright-cn/Mobile-Proxies/blob/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://bright.cn/proxy-types/mobile-proxies?promo=github15)

## 概览
通过 Bright Data 的[移动代理网络](https://bright.cn/proxy-types/mobile-proxies)，像真实的移动用户一样访问互联网，提供来自全球的数百万 3G、4G 和 5G IP。

- **7,000,000+ 移动 IP**
- **3G/4G/5G 移动 IP**
- **99.99% 正常运行时间，提供全天候支持**
- **地理位置定位（免费）**

## 核心功能
- **全球覆盖**：访问遍布[195 个国家](https://bright.cn/locations)的移动 IP。
- **高成功率**：在数据采集和测试任务中达到高达 99.9% 的成功率。
- **真实移动连接**：移动 IP 来自真实设备和可靠网络。
- **无限扩展**：支持并发会话和高可用性基础设施。
- **运营商级别定位**：按特定运营商定位，获取深入、准确的见解。

## 定价方案
- **按需支付**：$8.4/GB，无月度承诺。
- **月度订阅**：
  - **69 GB**：$7.14/GB，总计 $499/月 + 增值税。
  - **158 GB**：$6.3/GB，总计 $999/月 + 增值税。
  - **339 GB**：$5.88/GB，总计 $1999/月 + 增值税。
  - **企业方案**：提供定制的价格和套餐。

立即注册，首次充值即可享受最高 $500 的等额奖励！

## 开始使用移动代理
1. **开始免费试用**：无需信用卡。
2. **集成**：通过 API 或 Bright Data 控制面板管理 IP 和配置。
3. **支持的语言**：提供 Python、Java、C#、Node.js 和 Shell 的快速入门示例。

## 代码示例

### Python

```python
import sys

# Replace '[your customerID]', 'mobile', and '[your password]' with your actual Bright Data customer ID, zone, and password
if sys.version_info[0] == 2:
    import six
    from six.moves.urllib import request
    opener = request.build_opener(
        request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-mobile:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-mobile:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())

if sys.version_info[0] == 3:
    import urllib.request
    opener = urllib.request.build_opener(
        urllib.request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-mobile:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-mobile:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())
```

### Java

```java
package example;

import org.apache.http.HttpHost;
import org.apache.http.client.fluent.*;

public class Example {
    public static void main(String[] args) throws Exception {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        HttpHost proxy = new HttpHost("brd.superproxy.io", 22225);
        String res = Executor.newInstance()
            .auth(proxy, "brd-customer-[your customerID]-zone-mobile", "[your password]")
            .execute(Request.Get("https://geo.brdtest.com/mygeo.json").viaProxy(proxy))
            .returnContent().asString();
        System.out.println(res);
    }
}
```

### C#

```c#
using System;
using System.Net;

class Example
{
    static void Main()
    {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        var client = new WebClient();
        client.Proxy = new WebProxy("brd.superproxy.io:22225");
        client.Proxy.Credentials = new NetworkCredential("brd-customer-[your customerID]-zone-mobile", "[your password]");
        Console.WriteLine(client.DownloadString("https://geo.brdtest.com/mygeo.json"));
    }
}
```

### Node.js

```node.js
require('request-promise')({
    url: 'https://geo.brdtest.com/mygeo.json',
    proxy: 'http://brd-customer-[your customerID]-zone-mobile:"[your password]"@brd.superproxy.io:22225',
})
.then(function(data){ console.log(data); },
    function(err){ console.error(err); });
```

### Shell 

```shell
# Replace '[your customerID]' and '[your password]' with your actual credentials
curl --proxy brd.superproxy.io:22225 --proxy-user brd-customer-[your customerID]-zone-mobile:[your password] -k "https://geo.brdtest.com/mygeo.json"
```

## 集成
我们的移动代理可无缝集成到流行工具和框架中：

- [**Puppeteer**](https://bright.cn/integration/puppeteer)
- [**Selenium**](https://bright.cn/integration/selenium)
- [**Playwright**](https://bright.cn/integration/playwright)
- [**AdsPower**](https://bright.cn/integration/adspower)
- [**MultiLogin**](https://bright.cn/integration/multilogin)

## 使用场景
移动代理的常见应用包括：

- [**电商**](https://bright.cn/use-cases/ecommerce)：跟踪价格和产品库存。
- [**社交媒体**](https://bright.cn/use-cases/social-media-for-marketing)：监测趋势和用户参与度。
- [**房地产**](https://bright.cn/use-cases/real-estate)：收集房源数据。
- [**旅游**](https://bright.cn/use-cases/travel)：比较不同地点的旅游优惠。

## 常见问题

### 什么是移动代理？
移动代理通过真实运营商提供的移动 IP 路由流量，从而实现通过移动网络访问互联网。

### 移动代理有哪些用途？
移动代理通常用于广告验证、移动应用测试、基于位置的数据采集、社交媒体监测等多种场景。

### 为什么要使用移动代理？
移动代理具有高度的匿名性，不易被检测到，可提供与真实用户相同的移动网络数据访问。

### 你们提供 5G 移动代理吗？
是的，Bright Data 提供快速且安全的 5G 移动代理。

### 可以选择哪些移动运营商的 IP？
我们提供多种热门运营商的 IP，包括 [AT&T](https://bright.cn/solutions/att-proxy)、[T-Mobile](https://bright.cn/solutions/t-mobile-proxy)、[Verizon](https://bright.cn/solutions/verizon-proxy) 以及其他全球运营商的 IP。

### 移动代理合法吗？
是的，Bright Data 的移动代理符合包括 GDPR 和 CCPA 在内的所有相关法律，确保隐私和合法使用。

### 你们提供美国的移动代理吗？
是的，我们提供包括 AT&T 和 T-Mobile 等主要运营商 IP 的美国移动代理，以及全球范围内的移动代理。

### 可以按国家和城市选择移动 IP 吗？
可以，Bright Data 的移动代理网络支持按特定国家和城市定位。

### Bright Data 的移动代理是如何获取的？
Bright Data 与应用开发者合作，通过他们集成我们的 SDK，让用户选择共享移动 IP，以换取无广告体验或应用升级等福利。
