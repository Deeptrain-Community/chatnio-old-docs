---
description: API Key 中转
---

# 🌟 Key 中转

将接入点 [https://api.openai.com](https://api.openai.com) 更改为 [https://api.chatnio.net](https://api.chatnio.net) 即可使用

1. **支持 SSE 流式传输**
2. **多模型兼容** 不止 OpenAI 模型！其他模型格式相同 其他支持模型参考 [ai-mo-xing-ji-ji-fei.md](../../ai-mo-xing-ji-ji-fei.md "mention")
3. **Token 计算功能**



在 OpenAI API 原生适配的基础上，我们增加了更多扩展参数：

* Nio Point 费用计算&#x20;
* 流式传输 Token 计算

{% code lineNumbers="true" fullWidth="false" %}
```json
Example Response:
{
    "id": "...", // request id
    "object": "chat.completion",
    "created": 1696593899709, // time stamp
    "model": "gpt-4-32k" // request model, like spark-desk, bing-creative, claude-1 and etc.
    "choices": [
        ...
    ],
    "usage": {
        "prompt_tokens": 1322,
        "completion_tokens": 123,
        "total_tokens": 1445
    },
    "quota": 82.34 // quota usage
}
```
{% endcode %}

