---
description: 生成卡片
---

# 🍏 卡片

![](https://i.chatnio.net/?message=hi)

```markdown
![image](https://i.chatnio.net/?message=hi)
```

{% swagger method="get" path="/" baseUrl="https://i.chatnio.net" summary="生成卡片" %}
{% swagger-description %}
生成卡片，如 _https://i.chatnio.net/?message=hi_
{% endswagger-description %}

{% swagger-parameter in="query" name="message" type="String" required="true" %}
内容
{% endswagger-parameter %}

{% swagger-parameter in="query" name="theme" type="String" %}
主题 (**light** _默认_, **dark**)
{% endswagger-parameter %}

{% swagger-parameter in="query" name="web" type="Boolean" %}
是否开启联网功能（默认开启）
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="SVG Card" %}

{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="Rate Limit" %}

{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}

{% endswagger-response %}
{% endswagger %}
