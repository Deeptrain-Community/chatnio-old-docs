# 👋 快速开始

## 获取 API Key

在 chatnio 登录后，您可以在右上角头像下拉菜单中，生成 API Key。复制 API Key，这将会在下面的介绍中使用。

> 注意，请妥善保管您的 API Key！请不要在公开环境（如 GitHub 公开仓库）中泄露 API Key！

## 下载库



{% tabs %}
{% tab title="RESTful API" %}
使用 RESTful 接口无需进行此步骤
{% endtab %}

{% tab title="Node" %}
```sh
npm install --save chatnio-api
```
{% endtab %}

{% tab title="Python" %}
```sh
pip install -U chatnio-api
```
{% endtab %}

{% tab title="Go" %}
```sh
go get https://github.com/deeptrain-community/chatnio-api-go
```
{% endtab %}
{% endtabs %}

## 初始化

进行请求时，我们需要您的Key进行身份验证和配额计算。

{% tabs %}
{% tab title="RESTful API" %}
设置请求头：

| Header        | Value        |
| ------------- | ------------ |
| Authorization | Your API Key |
{% endtab %}

{% tab title="Node" %}
```javascript
// require the chatnio-api module and set it up with your API key
const nio = require("chatnio-api");
nio.setKey("your-api-key");
```
{% endtab %}

{% tab title="Python" %}
```python
# Set your API key before making the request
import nio
nio.setKey("your-api-key")

# get key from env:
# nio.setKeyFromEnv("env-name")
```
{% endtab %}

{% tab title="Go" %}

{% endtab %}
{% endtabs %}

## &#x20;创建第一个请求

{% tabs %}
{% tab title="RESTful API" %}

{% endtab %}

{% tab title="Node" %}

{% endtab %}

{% tab title="Python" %}

{% endtab %}

{% tab title="Go" %}

{% endtab %}
{% endtabs %}
