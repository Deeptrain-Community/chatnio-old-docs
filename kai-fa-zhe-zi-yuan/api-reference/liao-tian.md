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
是否开启联网功能（默认**关闭**）
{% endswagger-parameter %}

{% swagger-parameter in="body" name="type" type="String" %}
默认 **chat** 即可
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

#### 连接示例

<pre class="language-json"><code class="lang-json">> WEBSOCKET wss://api.chatnio.net/chat

* CONNECTION OPEN

<strong>> SEND {"token":"sk-...","id":-1}
</strong><strong>> SEND {"type": "chat", "message": "hi", "web": false, "model": "claude-2-100k", "ignore_context": false}
</strong><strong>&#x3C; RECV {"quota": 0, "keyword": "", "message": "Hello", "end": false}
</strong><strong>&#x3C; RECV {"quota": 0.0034000003, "keyword": "", "message": "!", "end": false}
</strong><strong>&#x3C; RECV {"quota": 0.0034000003, "keyword": "", "message": "", "end": true}
</strong><strong>
</strong><strong>* CONNECTION CLOSE
</strong><strong>* CONNECTION CLOSE BY PEER
</strong></code></pre>

