# 🎁 订阅和礼包

## 查询订阅

{% swagger method="get" path="/subscription" baseUrl="https://api.chatnio.net" summary="查询订阅，返回是否订阅和订阅剩余天数" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="Query Successfully" %}
<pre class="language-json"><code class="lang-json">{
    "status":        true,
<strong>    "is_subscribed": true,
</strong>    "expired":       11
}
</code></pre>
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}

{% endswagger-response %}
{% endswagger %}

## 购买订阅

{% swagger method="post" path="/subscribe" baseUrl="https://chatnio.net" summary="购买订阅，从 Deeptrain 钱包扣除余额，返回订阅状态" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="month" type="Integer" required="true" %}
介于 0 \~ 999 之间的整数
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Pay Successfully" %}
```json
{
    "status": false,
    "error": "success"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="Unauthorized" %}

{% endswagger-response %}
{% endswagger %}

