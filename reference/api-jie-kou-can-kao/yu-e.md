# 💰 余额

## 查询余额

{% swagger method="get" baseUrl="https://api.chatnio.net" path="/quota" summary="" %}
{% swagger-description %}
查询余额，返回余额（浮点数）
{% endswagger-description %}

{% swagger-response status="200" description="Pet successfully created" %}
```json
{
    "status": true,
    "quota": 1.26
}
```
{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %}
{% endswagger %}



## 购买余额

{% swagger src="https://petstore.swagger.io/v2/swagger.json" path="/pet" method="put" %}
[https://petstore.swagger.io/v2/swagger.json](https://petstore.swagger.io/v2/swagger.json)
{% endswagger %}
