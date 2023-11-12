---
description: 常见问题 Q & A
---

# 😲 常见问题解答

### 🍀 AI 模型相关

#### 1> GPT-4, GPT-4V, GPT-4 DALLE, GPT-4 ALL, GPT-4 32k 都有什么区别？

1. **GPT-4** 和 **GPT-4 32k** 为纯文字模型, 对接官方 API，普通 GPT-4 上下文长度为 8K Tokens，32K 上下文长度顾名思义为 32K Tokens, 32K 不常用，价格约为 GPT-4 的两倍，仅作为大数据分析情况使用，正常使用 GPT-4 即可。
2. **GPT-4V**, **GPT-4 DALLE** 为多模态模型,由 Plus 逆向而成, 4V可以识别图片，DALLE3 可生成图片。因其为 Plus 逆向，有时会有额度不足的情况，出现 500 为正常现象，等 Plus 账号池额度恢复即可（三小时以内）。
3. **GPT-4 ALL** 为 Alpha 号逆向而成，同时兼顾 DALLE3 绘图功能和识别图片能力，上下文长度可达 128k

#### 2> Claude 100k 是什么？

Claude 100k 支持 100k 上下文，支持大文本解析等功能，从价格，稳定性，并发考虑来看是不错的选择。

#### 3> 为什么我选 GPT-4 模型，但是他说是基于 GPT-3 架构？

此为正常现象，GPT-4会回答自己为“基于 GPT-3 架构开发（还不是回答 GPT3.5架构）”， 您可以提问诸如“_鲁迅为什么暴打周树人, 打鸟问题，Tile T2 Project_” 等问题综合辨别市面上的真假 GPT-4 模型。3.5 会开始胡编模式说为两个人，4 会正常回答。



### ✨ Key 中转相关



1. **ChatGPT Next Web**

> 您可以直接使用 [nextweb.chatnio.net](https://nextweb.chatnio.net)

1. API Key 从下拉菜单中的 **API 设置** 中获取
2. 接口地址填写 **https://api.chatnio.net**



2. **OpenAI SDKs** (以Python为例)

```python
import openai

openai.base_url = "https://api.chatnio.net/v1/"
openai.api_key = "<Your Api-Key>"
```



3. **One API**

* 设置 **OpenAI** 格式，代理地址为 **https://api.chatnio.net**

3. **LobeChat**&#x20;

> 当前不支持 Function Call 功能，敬请期待



4. **ChatBox**

* 代理设置为 **https://api.chatnio.net**



5. **ChatGPT Sidebar**

* 接入点设置为 **https://api.chatnio.net**



6. **EasyCode**

* 自定义服务器地址设置为 **https://api.chatnio.net/v1/chat/completions**



7. **Fystart**

* OpenAI 接入点设置为 **wss://api.chatnio.net**

