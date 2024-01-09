---
description: 使用 Chat Nio 中转 API 兼容第三方常见项目（订阅配额不适用于中转 API）
---

# 🛠 常见项目配置

### :gear: 工具设置

{% hint style="info" %}
此为 chatnio.net 官方站的设置，其他站点根据下列配置参考

（非前后端分离部署的 API 端点为 /api）
{% endhint %}

1. **ChatGPT Next Web**

> 官站也可以直接使用 [nextweb.chatnio.net](https://nextweb.chatnio.net)

* API Key 从下拉菜单中的 **API 设置** 中获取
* 接口地址填写 **https://api.chatnio.net**



2. **OpenAI SDKs** (以Python为例)

```python
import openai

openai.base_url = "https://api.chatnio.net/v1/"
openai.api_key = "<Your Api-Key>"
```

3. **One API**

* 设置 **OpenAI** 格式，代理地址为 **https://api.chatnio.net**

3. **LobeChat**

* 设置中更改接入点为 **https://api.chatnio.net/v1**

4. **ChatBox**

* 代理设置为 **https://api.chatnio.net**

5. **GPT-Academic**

* 配置中自定义 Key 格式设置为：`CUSTOM_API_KEY_PATTERN = "sk-[a-zA-Z0-9]{64}$"`
* 配置中增加 URL 重定向：`API_URL_REDIRECT = {"https://api.openai.com/v1/chat/completions": "https://api.chatnio.net/v1/chat/completions"}`
* 填写 API Key 至 `API_KEY`

6. **ChatGPT Sidebar**

* 接入点设置为 **https://api.chatnio.net**

7. **EasyCode**

* 自定义服务器地址设置为 **https://api.chatnio.net/v1/chat/completions**

8. **Fystart**

* OpenAI 接入点设置为 **wss://api.chatnio.net**
