# 💰 余额

{% hint style="info" %}
&#x20;1 CNY = 10 Nio Point
{% endhint %}

## 查询余额

{% swagger method="get" baseUrl="https://api.chatnio.net" path="/quota" summary="查询余额，返回余额（浮点数）" %}
{% swagger-description %}
返回余额（浮点数）
{% endswagger-description %}

{% swagger-response status="200" description="Query successfully" %}
```json
{
    "status": true,
    "quota": 12.6
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="Unauthorized" %}

{% endswagger-response %}
{% endswagger %}



## 购买余额

{% swagger method="post" path="/buy" baseUrl="https://api.chatnio.net" summary="扣除 Deeptrain 钱包余额，返回支付状态" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="quota" type="Integer" required="true" %}
介于 1 \~ 99999 之间的整数
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Pay Successfully" %}
```json
{
    "status": true,
    "error": "success"
}
```
{% endswagger-response %}

{% swagger-response status="200: OK" description="Not Enough Money" %}
```json
{
    "status": false,
    "error": "not enough money"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="Unauthorized" %}

{% endswagger-response %}
{% endswagger %}

