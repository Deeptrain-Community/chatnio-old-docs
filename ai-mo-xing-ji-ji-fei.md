# 🧐 AI 模型计费

[chatnio官方站](https://chatnio.net/) 有两种计费方式。一种是随用随付的弹性计费，一种是订阅计划。**其他站点请参阅其站点的信息，与官方站计费无关。**

下面是弹性计费方式的详细价格表。请到chatnio官方站查看订阅计划的详细信息。

{% hint style="info" %}
**1 CNY = 10 Nio 点数。** (如模型请求 1 次计费 0.05 点数，即计费 0.005 元)

**订阅的按次配额在 API 中转中无法适用，中转仅支持弹性计费。**
{% endhint %}

### OpenAI / Azure OpenAI

<table><thead><tr><th>模型</th><th>费率</th><th width="126">问题 Token (点数 / 1k token)</th><th>回答 Token (点数 / 1k token)</th></tr></thead><tbody><tr><td>gpt-3.5-turbo (0301, 0613)</td><td>1 元 1 刀 (<a href="https://openai.com/pricing">官网</a> 7 分之一)</td><td>0.015</td><td>0.02</td></tr><tr><td>gpt-3.5-turbo-1106</td><td>1 元 1 刀 (<a href="https://openai.com/pricing">官网</a> 7 分之一)</td><td>0.01</td><td>0.02</td></tr><tr><td>gpt-3.5-turbo-16k</td><td>1 元 1 刀 (<a href="https://openai.com/pricing">官网</a> 7 分之一)</td><td>0.03</td><td>0.04</td></tr><tr><td>gpt-4 (0301, 0613)</td><td>1 元 1 刀 (<a href="https://openai.com/pricing">官网</a> 7 分之一)</td><td>0.3</td><td>0.6</td></tr><tr><td><p>gpt-4-1106-preview, </p><p>gpt-4-0125-preview,</p><p>gpt-4-turbo-preview,</p><p>gpt-4-vision-preview</p></td><td>1 元 1 刀 (<a href="https://openai.com/pricing">官网</a> 7 分之一)</td><td>0.1</td><td>0.3</td></tr><tr><td>gpt-4-32k</td><td>1 元 1 刀 (<a href="https://openai.com/pricing">官网</a> 7 分之一)</td><td>0.6</td><td>1.2</td></tr><tr><td>azure-gpt-3.5-turbo</td><td>0.4 元 1 刀 (官网 17 分之一)</td><td>0.006</td><td>0.008</td></tr><tr><td>azure-gpt-3.5-turbo-16k</td><td>0.4 元 1 刀 (官网 17 分之一)</td><td>0.012</td><td>0.016</td></tr><tr><td>azure-gpt-4</td><td>0.8 元 1 刀 (官网 9 分之一)</td><td>0.240</td><td>0.480</td></tr><tr><td>azure-gpt-4-32k</td><td>0.8 元 1 刀 (官网 9 分之一)</td><td>0.480</td><td>0.960</td></tr><tr><td>gpt-3.5-turbo-fast</td><td><a href="https://openai.com/pricing">官网</a> 6折</td><td>0.105 * 0.6</td><td>0.215 * 0.6</td></tr><tr><td>gpt-3.5-turbo-16k-fast</td><td><a href="https://openai.com/pricing">官网</a> 6折</td><td>0.21 * 0.6</td><td>0.43 * 0.6</td></tr><tr><td>dalle, dall-e-2, dall-e-3 </td><td>请参见下方 <strong>AI 绘图</strong></td><td>-</td><td>-</td></tr></tbody></table>

{% hint style="warning" %}
GPT 3.5 Fast 系列支持高并发，保证稳定性。



DALLE-2, DALLE-3, GPT-4 Vision Preview 已做好格式兼容，按照通用格式调用即可（在任何地方输入 url 即可），无需再适配进行格式。
{% endhint %}

### AI 绘图



<table><thead><tr><th width="194">模型</th><th>费率</th><th>价格（点数）</th><th width="234">信息</th></tr></thead><tbody><tr><td>dalle, dall-e-2</td><td>1 元 1 刀 (<a href="https://openai.com/pricing">官网</a> 7 分之一)</td><td>0.18</td><td>512x512</td></tr><tr><td>dall-e-3</td><td><a href="https://openai.com/pricing">官网</a> 6折</td><td>3</td><td>HD 1024x1024</td></tr><tr><td>midjourney</td><td><a href="https://docs.midjourney.com/docs/plans">官网</a>平均计费</td><td>1</td><td>Relax 模式</td></tr><tr><td>midjourney-fast</td><td><a href="https://docs.midjourney.com/docs/plans">官网</a>平均计费</td><td>2</td><td>Fast 模式</td></tr><tr><td>midjourney-turbo</td><td><a href="https://docs.midjourney.com/docs/plans">官网</a>平均计费</td><td>5</td><td>Turbo 模式</td></tr><tr><td>stable-diffusion</td><td>算力平均值</td><td>0.25</td><td>Stable Diffusion XL, POE 逆向 + Hugging Face</td></tr></tbody></table>

### Claude

<table><thead><tr><th>模型</th><th>费率</th><th width="128">问题 Token (点数 / 1k token)</th><th>回答 Token (点数 / 1k token)</th></tr></thead><tbody><tr><td><p>claude-1-100k, claude-1, </p><p>claude-1.3, </p><p>cluade-slack (废弃)</p></td><td>对齐<a href="https://anthropic.com/pricing/">官网</a>计费</td><td>0.08</td><td>0.27</td></tr><tr><td>claude-2, claude-2.1</td><td>对齐<a href="https://anthropic.com/pricing/">官网</a>计费</td><td>0.8</td><td>2.7</td></tr></tbody></table>

{% hint style="info" %}
Claude 2 为 100k 上下文，Claude 2.1 为 200k 上下文，Claude 全系并发较低，出现 403, 503 等报错为正常上游速率限制情况。

Claude Slack 因为 Slack 政策调整现已关闭使用。
{% endhint %}

### SparkDesk 讯飞星火

<table><thead><tr><th>模型</th><th>费率</th><th width="135">问题 Token (点数 / 1k token)</th><th>回答 Token (点数 / 1k token)</th></tr></thead><tbody><tr><td>spark-desk-v1.5</td><td>对齐<a href="https://xinghuo.xfyun.cn/sparkapi">官网</a>计费</td><td>0.15</td><td>0.15</td></tr><tr><td>spark-desk-v2</td><td>对齐<a href="https://xinghuo.xfyun.cn/sparkapi">官网</a>计费</td><td>0.3</td><td>0.3</td></tr><tr><td>spark-desk-v3</td><td>对齐<a href="https://xinghuo.xfyun.cn/sparkapi">官网</a>计费</td><td>0.3</td><td>0.3</td></tr></tbody></table>

### ChatGLM 智谱清言

<table><thead><tr><th>模型</th><th>费率</th><th width="147">问题 Token (点数 / 1k token)</th><th>回答 Token (点数 / 1k token)</th></tr></thead><tbody><tr><td>zhipu-chatglm-turbo</td><td>对齐<a href="https://open.bigmodel.cn/pricing">官网</a>计费</td><td>0.05</td><td>0.05</td></tr><tr><td>zhipu-chatglm-pro（废弃）</td><td>对齐<a href="https://open.bigmodel.cn/pricing">官网</a>计费</td><td>0.1</td><td>0.1</td></tr><tr><td>zhipu-chatglm-std（废弃）</td><td>对齐<a href="https://open.bigmodel.cn/pricing">官网</a>计费</td><td>0.05</td><td>0.05</td></tr><tr><td>zhipu-chatglm-lite（废弃）</td><td>对齐<a href="https://open.bigmodel.cn/pricing">官网</a>计费</td><td>0.05</td><td>0.05</td></tr></tbody></table>

### DashScope 通义千问

<table><thead><tr><th>模型</th><th>费率</th><th width="131">问题 Token (点数 / 1k token)</th><th>回答 Token (点数 / 1k token)</th></tr></thead><tbody><tr><td>qwen-plus</td><td>对齐<a href="https://help.aliyun.com/zh/dashscope/developer-reference/tongyi-thousand-questions-metering-and-billing">官网</a>计费</td><td>0.2</td><td>0.2</td></tr><tr><td>qwen-plus-net</td><td>对齐<a href="https://help.aliyun.com/zh/dashscope/developer-reference/tongyi-thousand-questions-metering-and-billing">官网</a>计费</td><td>0.2</td><td>0.2</td></tr><tr><td>qwen-turbo</td><td>对齐<a href="https://help.aliyun.com/zh/dashscope/developer-reference/tongyi-thousand-questions-metering-and-billing">官网</a>计费</td><td>0.08</td><td>0.08</td></tr><tr><td>qwen-turbo-net</td><td>对齐<a href="https://help.aliyun.com/zh/dashscope/developer-reference/tongyi-thousand-questions-metering-and-billing">官网</a>计费</td><td>0.08</td><td>0.08</td></tr></tbody></table>

### Google Gemini / PaLM2

| 模型                                                                | 回答 Token (点数 / 次数) |
| ----------------------------------------------------------------- | ------------------ |
| <p>chat-bison-001,</p><p>gemini-pro, </p><p>gemini-pro-vision</p> | 0.05 / 次           |

{% hint style="info" %}
Google PaLM2 (chat-bision-001) 不支持包括中文在内的语言并且会频繁出现编码问题，Google 几乎已废弃该模型，推荐使用 Gemini (gemini 返回同为“伪”流式传输)。
{% endhint %}

### New Bing

| 模型            | 回答 Token (点数 / 次数) |
| ------------- | ------------------ |
| bing-creative | 0.1 / 次            |
| bing-balanced | 0.1 / 次            |
| bing-precise  | 0.1 / 次            |

{% hint style="info" %}
New Bing 为逆向模型，不保证并发，出现错误为正常现象。
{% endhint %}

### Meta LLaMa

<table><thead><tr><th>模型</th><th>费率</th><th width="138">问题 Token (点数 / 1k token)</th><th>回答 Token (点数 / 1k token)</th></tr></thead><tbody><tr><td><p>llama-2-70b</p><p>code-llama-34b</p></td><td>算力平均值</td><td>0.25</td><td>0.25</td></tr><tr><td><p>llama-2-13b</p><p>llama-2-7b</p><p>code-llama-13b</p><p>code-llama-7b</p></td><td>算力平均值</td><td>0.1</td><td>0.1</td></tr></tbody></table>

{% hint style="info" %}
LLaMa 模型不保证高速和稳定性，吐字速度随当前可用性能影响
{% endhint %}

### 腾讯混元

<table><thead><tr><th>模型</th><th>费率</th><th width="138">问题 Token (点数 / 1k token)</th><th>回答 Token (点数 / 1k token)</th></tr></thead><tbody><tr><td>hunyuan</td><td>对齐<a href="https://cloud.tencent.com/document/product/1729/97731">官网</a>计费</td><td>1</td><td>1</td></tr></tbody></table>

### 360 智脑

<table><thead><tr><th>模型</th><th>费率</th><th width="138">问题 Token (点数 / 1k token)</th><th>回答 Token (点数 / 1k token)</th></tr></thead><tbody><tr><td>360-gpt-v9</td><td>对齐<a href="https://ai.360.com/platform/limit">官网</a>计费</td><td>0.12</td><td>0.12</td></tr></tbody></table>

### **百川 AI**

<table><thead><tr><th>模型</th><th>费率</th><th width="138">问题 Token (点数 / 1k token)</th><th>回答 Token (点数 / 1k token)</th></tr></thead><tbody><tr><td>baichuan-53b</td><td>对齐<a href="https://platform.baichuan-ai.com/price">官网</a>计费</td><td>0.2</td><td>0.2</td></tr></tbody></table>

### 火山方舟（抖音豆包）

<table><thead><tr><th>模型</th><th>费率</th><th width="138">问题 Token (点数 / 1k token)</th><th>回答 Token (点数 / 1k token)</th></tr></thead><tbody><tr><td>skylark-lite-public</td><td>对齐<a href="https://www.volcengine.com/docs/82379/1099320">官网</a>计费</td><td>0.04</td><td>0.04</td></tr><tr><td>skylark-plus-public</td><td>对齐<a href="https://www.volcengine.com/docs/82379/1099320">官网</a>计费</td><td>0.08</td><td>0.08</td></tr><tr><td>skylark-pro-public</td><td>对齐<a href="https://www.volcengine.com/docs/82379/1099320">官网</a>计费</td><td>0.11</td><td>0.11</td></tr><tr><td>skylark-chat</td><td>对齐<a href="https://www.volcengine.com/docs/82379/1099320">官网</a>计费</td><td>0.11</td><td>0.11</td></tr></tbody></table>

## 最低余额限制

为了防止超出余额的部分过多，同时为了防止滥用，Chat Nio 设定了特定模型的最低余额预检，当小于该余额时，不可发起请求。

> 对于按照次数计费模型，最低余额为单次调用费用。（如：模型 0.1 点数 / 次, 最低可调用点数余额为 0.1）
>
> 对于按照 Token 计费模型，最低余额为 1K 输入 Token 费用 + 1K 输出 Token 费用。（如：模型输入输出均为 0.1 点数 / 1k tokens, 最低可调用点数余额为 0.1 + 0.1 = 0.2）
>
> 对于不计费模型，无最低余额限制。

