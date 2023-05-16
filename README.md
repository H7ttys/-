聊天机器人界面
Chatbot UI 是一个用于 AI 模型的开源聊天 UI。

看一个演示。

聊天机器人界面

更新
Chatbot UI 将随着时间的推移而更新。

期望经常改进。

接下来：

分享
“机器人”
部署
韦塞尔

使用 Vercel 托管您自己的聊天机器人 UI 实时版本。

使用 Vercel 部署

码头工人

本地构建：

docker build -t chatgpt-ui .
docker run -e OPENAI_API_KEY=xxxxxxxx -p 3000:3000 chatgpt-ui
从 ghcr 拉取：

docker run -e OPENAI_API_KEY=xxxxxxxx -p 3000:3000 ghcr.io/mckaywrigley/chatbot-ui:main
本地运行
1.克隆回购

git clone https://github.com/mckaywrigley/chatbot-ui.git
2.安装依赖

npm i
3.提供OpenAI API Key

使用您的 OpenAI API 密钥在存储库的根目录中创建一个 .env.local 文件：

OPENAI_API_KEY=YOUR_KEY
您可以设置OPENAI_API_HOST对官方 OpenAI 主机的访问受限或不可用的位置，从而允许用户根据他们的特定需求配置备用主机。

此外，如果您有多个 OpenAI 组织，您可以设置OPENAI_ORGANIZATION为指定一个。

4.运行应用

npm run dev
5. 使用它

您应该可以开始聊天了。

配置
部署应用程序时，可以设置以下环境变量：

环境变量	默认值	描述
OPENAI_API_KEY		用于 OpenAI 身份验证的默认 API 密钥
OPENAI_API_HOST	https://api.openai.com	基本 url，供 Azure 使用https://<endpoint>.openai.azure.com
OPENAI_API_TYPE	openai	API 类型，选项是openai或azure
OPENAI_API_VERSION	2023-03-15-preview	仅适用于 Azure OpenAI
AZURE_DEPLOYMENT_ID		Azure OpenAI 时需要，参考Azure OpenAI API
OPENAI_ORGANIZATION		您的 OpenAI 组织 ID
默认模型	gpt-3.5-turbo	用于新对话的默认模型，供 Azure 使用gpt-35-turbo
NEXT_PUBLIC_DEFAULT_SYSTEM_PROMPT	看这里	用于新对话的默认系统提示
NEXT_PUBLIC_DEFAULT_TEMPERATURE	1个	用于新对话的默认温度
GOOGLE_API_KEY		请参阅自定义搜索 JSON API 文档
GOOGLE_CSE_ID		请参阅自定义搜索 JSON API 文档
如果您不使用 提供 OpenAI API 密钥OPENAI_API_KEY，用户将必须提供自己的密钥。

如果您没有 OpenAI API 密钥，可以在此处获取。

接触
如果您有任何疑问，请随时在Twitter上联系 Mckay 。
