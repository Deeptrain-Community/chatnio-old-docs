---
description: 常见问题 Q & A
---

# ❓ 常见问题解答

### 🍀 AI 模型相关

#### 1> GPT-4, GPT-4V, GPT-4 DALLE, GPT-4 ALL, GPT-4 32k 都有什么区别？

1. **GPT-4** 和 **GPT-4 32k** 为纯文字模型, 对接官方 API，普通 GPT-4 上下文长度为 8K Tokens，32K 上下文长度顾名思义为 32K Tokens, 32K 不常用，价格约为 GPT-4 的两倍，仅作为大数据分析情况使用，正常使用 GPT-4 即可。
2. **GPT-4V**, **GPT-4 DALLE** 为多模态模型,由 Plus 逆向而成, 4V可以识别图片，DALLE3 可生成图片。因其为 Plus 逆向，有时会有额度不足的情况，出现 500 为正常现象，等 Plus 账号池额度恢复即可（三小时以内）。
3. **GPT-4 ALL** 为 Alpha 号逆向而成，同时兼顾 DALLE3 绘图功能和识别图片能力，上下文长度可达 128k

#### 2> Claude 100k 是什么？

Claude 100k 支持 100k 上下文，支持大文本解析等功能，从大文章理解能力考虑来看是不错的选择。

#### 3> 为什么我选 GPT-4 模型，但是他说是基于 GPT-3 架构？

此为正常现象，GPT-4会回答自己为“基于 GPT-3 架构开发（还不是回答 GPT3.5架构）”， 您可以提问诸如“_鲁迅为什么暴打周树人, 打鸟问题，Tile T2 Project_” 等问题综合辨别市面上的真假 GPT-4 模型。3.5 会开始胡编模式说为两个人，4 会正常回答。(此问题已过时）

**4> 如何计算 Token 消耗**

询问模型自己用了多少 token 是不可行的，模型只会得出错误答案。Token 计算方法请前往 OpenAI 官方 Token 计算器 [https://platform.openai.com/tokenizer](https://platform.openai.com/tokenizer) 进行计算，并乘以权重 _TokensPerMessage_ 参数（一般为 _3_）。

在一次请求中，输入 token 即为携带的历史的上下文（默认最多携带 8 轮上下文对话），输出token即为模型的回复。

Tokenizer 的计算方法请查看 OpenAI Cookbox，Chat Nio 的 Token 计费方式完全参照 OpenAI 官方进行，后端使用 Tiktoken Go 库进行计算。

{% embed url="https://github.com/openai/openai-cookbook/blob/main/examples/How_to_count_tokens_with_tiktoken.ipynb" %}
Tiktoken Notebook
{% endembed %}

{% embed url="https://github.com/pkoukk/tiktoken-go" %}
Tiktoken Go
{% endembed %}

{% embed url="https://github.com/Deeptrain-Community/chatnio/blob/main/utils/tokenizer.go" %}
Chat Nio 后端实现
{% endembed %}

### 🔨 常见报错原因列表

* 504 Gateway Timeout：网关超时，服务异常（常发生于服务器满负载运行时或者 CDN 网关超过最大 Timeout），请联系网站相关人员解决。
* 503 Service Unavailable：服务暂时不可用。常发生于上游流量过大无法提供服务（如 Poe 逆向）。
* 500 Internal Server Error：上游服务端异常 （如 OpenAI 受到的流量过大时拒绝服务）。
* 404 Not Found： 出现于逆向模型。如上文所述，会有逆向账户鉴权失败或者逆向库失效的情况，为正常现象，等恢复即可。
* 403 Forbidden：拒绝服务。速率限制，或者会有逆向账户额度不足的情况，等账号池额度恢复即可。
* 402 Payment Required：账号池轮询到了余额不足的账户，请刷新重试。
* 401 Unauthorized：账号池轮询到了被封禁 / 不存在的账户，请刷新重试。
* 400 Bad Request：错误请求。参数设置不正确，或者上下文 Token 大小超过该模型的最大上下文。

