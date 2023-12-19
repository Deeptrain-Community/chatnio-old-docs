---
description: 说明 ChatNio API 的使用方式。
cover: >-
  https://images.unsplash.com/photo-1607799279861-4dd421887fb3?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHw1fHxQcm9ncmFtbWluZyUyMEludGVyZmFjZXxlbnwwfHx8fDE2OTc4NjY4NzR8MA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# 🏃 API 快速入门

## AI 模型计费策略

**除了中转 Key 外**， **API**与通过**网页**使用的计费方式是相同的，本质上是相同的接口（如 `gpt-3.5-turbo-16k`, 网站免费，同理得 API 免费）。

**中转 Key 仅支持弹性计费。**参考下方弹性计费标准：

{% content-ref url="../ai-mo-xing-ji-ji-fei.md" %}
[ai-mo-xing-ji-ji-fei.md](../ai-mo-xing-ji-ji-fei.md)
{% endcontent-ref %}

## 获取 API Key

{% hint style="danger" %}
请妥善保管您的 API Key！请不要在公开环境（如 GitHub 公开仓库）中泄露 API Key！
{% endhint %}

在 chatnio 登录后，您可以在右上角头像下拉菜单中，生成 API Key。复制 API Key，这将会在下面的介绍中使用。

## 下一步

[Python SDK](https://github.com/Deeptrain-Community/chatnio-api-python)

[Nodejs SDK](https://github.com/Deeptrain-Community/chatnio-api-node)

[Golang SDK](https://github.com/Deeptrain-Community/chatnio-api-go)

## API 接口参考

{% content-ref url="api-reference/" %}
[api-reference](api-reference/)
{% endcontent-ref %}
