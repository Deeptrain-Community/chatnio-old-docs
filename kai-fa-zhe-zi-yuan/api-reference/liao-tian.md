# 😀 聊天

## 聊天

`CONNECT` `wss://api.chatnio.net/chat`

\[**WebSocket**] 聊天

#### Query Parameters

| Name                                    | Type    | Description                                          |
| --------------------------------------- | ------- | ---------------------------------------------------- |
| token<mark style="color:red;">\*</mark> | String  | API Key              |
| id<mark style="color:red;">\*</mark>    | String  | 对话 ID [dui-hua.md](dui-hua.md "mention") （新对话时参数为 **-1**） |

#### Request Body

| Name                                      | Type   | Description                                                              |
| ----------------------------------------- | ------ | ------------------------------------------------------------------------ |
| message<mark style="color:red;">\*</mark> | String | 消息                                                                       |
| model<mark style="color:red;">\*</mark>   | String | AI 模型 [ai-mo-xing-ji-ji-fei.md](../../ai-mo-xing-ji-ji-fei.md "mention") |
| web                                       | String | 是否开启联网功能（默认**关闭**）                                                       |
| type                                      | String | 默认 **chat** 即可, **stop** 为暂停输出, **restart** 为重新回答                        |

{% tabs %}
{% tab title="200: OK WebSocket Stream Response" %}
```json
{
    "message": " how", // chunk message
    "quota": 0.02, // quota usage
    "end": false // output status
}
```
{% endtab %}
{% endtabs %}

#### 连接示例

<pre class="language-json"><code class="lang-json">> WEBSOCKET wss://api.chatnio.net/chat

* CONNECTION OPEN

<strong>> SEND {"token":"sk-...","id":-1}
</strong><strong>> SEND {"type": "chat", "message": "hi", "web": false, "model": "gpt-4", "ignore_context": false}
</strong><strong>&#x3C; RECV {"quota": 0, "keyword": "", "message": "Hello", "end": false}
</strong><strong>&#x3C; RECV {"quota": 0.0034000003, "keyword": "", "message": "!", "end": false}
</strong><strong>&#x3C; RECV {"quota": 0.0034000003, "keyword": "", "message": "", "end": true}
</strong>
<strong>* CONNECTION CLOSE
</strong><strong>* CONNECTION CLOSE BY PEER
</strong></code></pre>
