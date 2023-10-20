---
description: 生成项目
---

# 💡 项目生成

{% hint style="info" %}
项目生成功能基于预设完成，不保证成功率和稳定性
{% endhint %}

{% swagger method="connect" path="/generation/create" baseUrl="wss://api.chatnio.net" summary="生成项目" %}
{% swagger-description %}
\[**WebSocket**] 生成项目
{% endswagger-description %}

{% swagger-parameter in="body" name="token" type="String" required="true" %}
JWT Token / API Key (匿名: **anonymous**)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="prompt" type="String" required="true" %}
消息
{% endswagger-parameter %}

{% swagger-parameter in="body" name="model" type="String" required="true" %}
AI 模型 [ai-mo-xing-ji-ji-fei.md](../../../ai-mo-xing-ji-ji-fei.md "mention")
{% endswagger-parameter %}

{% swagger-response status="201: Created" description="WebSocket Stream Response" %}
```json
{
    "message": "Hello! ", // preview message
    "end": false,
    "quota": 0.0,
    "error": "",
    "hash": ""  // generation result (when end is true)
}
```
{% endswagger-response %}
{% endswagger %}

## 下载项目

#### tar.gz 格式：

<pre class="language-url"><code class="lang-url"><strong>https://api.chatnio.net/generation/download/tar?hash=...
</strong></code></pre>

#### zip 格式：

```uri
https://api.chatnio.net/generation/download/zip?hash=...
```
