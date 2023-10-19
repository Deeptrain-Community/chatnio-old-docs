# 😀 聊天



{% swagger method="connect" path="/chat" baseUrl="wss://api.chatnio.net" summary="聊天" %}
{% swagger-description %}
\[**WebSocket**] 聊天
{% endswagger-description %}

{% swagger-parameter in="query" name="token" type="String" required="true" %}
JWT Token / API Key (匿名: **anonymous**)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="id" type="String " required="true" %}
对话 ID [dui-hua.md](dui-hua.md "mention") （新建：**-1**）
{% endswagger-parameter %}

{% swagger-parameter in="body" name="message" type="String" required="true" %}
消息
{% endswagger-parameter %}

{% swagger-parameter in="body" name="model" type="String" required="true" %}
AI 模型 [ai-mo-xing-ji-ji-fei.md](../../ai-mo-xing-ji-ji-fei.md "mention")
{% endswagger-parameter %}

{% swagger-parameter in="body" name="web" type="String" %}
是否开启联网功能（默认**开启**）
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="WebSocket Stream Response" %}
```json
{
    "message": " how",
    "keyword": "", // enable when [web] is true
    "quota": 0.02,
    "end": false
}
```
{% endswagger-response %}
{% endswagger %}
