# ⏱ 对话

## 历史对话

{% swagger method="get" path="/conversation/list" baseUrl="https://api.chatnio.net" summary="列出对话" %}
{% swagger-description %}
列出近 100 次对话
{% endswagger-description %}

{% swagger-response status="200: OK" description="Request Successfully" %}
```json
{
    "status": true,
    "message": "",
    "data": [
        {
            "id": 1,
            "user_id": 1,
            "name": "new chat",
            "message": null,
            "model": "spark-desk" // latest model
            "enable_web": true // latest option
        }, 
        ...
    ]
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="Unauthorized" %}

{% endswagger-response %}
{% endswagger %}

## 获取对话

{% swagger method="get" path="/conversation/load" baseUrl="https://api.chatnio.net" summary="获取单个对话内容" %}
{% swagger-description %}
获取单个对话内容, 如 _https://api.chatnio.net/conversation?id=1_
{% endswagger-description %}

{% swagger-parameter in="query" name="id" type="Integer" required="true" %}
会话 ID (整数)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Request Successfully" %}
```json
{
    "status": true,
    "message": "success",
    "data": {
        "id": 1,
        "user_id": 1,
        "name": "what is chatnio",
        "message": [
            {"role": "system": content: "Respond with accurate content in the user's language"},
            {"role": "user", "content": "what is chatnio"},
            {"role": "assistant", "content": "As an AI language model, ..."},
            ...
        ],
        "model": "gpt-3.5-turbo-0613" // latest model
        "enable_web": false // latest option
    }, 
}
```
{% endswagger-response %}

{% swagger-response status="200: OK" description="Conversation Not Found" %}
```json
{
    "status": false,
    "message": "conversation not found"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}
{% endswagger %}
