# draft

实在累了, 做个简单的记录, 步骤, 用到的资源, 难点, 以及成果啥的.

懒得跑一编啥ai润色了, 简简单单拿vsc对个md格式化文档就完事了.

## 1

先是从[Telegram Bot but 2023](https://www.youtube.com/watch?v=vZtm1wuA2yc)

跑出来了, 然后`/`命令可以运行, 但是其他的涉及到filter更新啥的就不行了.

## 2

然后我向上搜索源头, 去了[python-telegram-bot的GitHub主页](https://github.com/python-telegram-bot/python-telegram-bot/wiki/Extensions---Your-first-Bot), 照着教程, 顺利在本地实现了教程涉及的所有功能.

## 3

然后我去打开yihong0618的[tg_bot_collections](https://github.com/yihong0618/tg_bot_collections), 发现用的是另一个`import telebot`.

我去搜这个指令, 李逵李鬼一大圈. 我通过requirements.txt 核对是`pip install pyTelegramBotAPI`,

从[pypi](https://pypi.org/project/pyTelegramBotAPI/)找到去了[GitHub](https://github.com/eternnoir/pyTelegramBotAPI).

然后简单地水了个echo bot, 也顺利运行了.

## 4

然后想着搓下GROQ的bot(优雅点地将: 通过实践API来获得实践经验), 但查看代码发现这就是里面的llama bot嘛, 已经做完了.

我于是简单地弄开了个`tg_bot_collections_lite`文件夹, 目标是简单地在本地跑起来, 同时兼容[tg_bot_collections](https://github.com/yihong0618/tg_bot_collections).

手动写了个`.env`简单地获取和输入token, 也顺利运行了.

## 5

我想着, 都到这里, 感觉不弄点啥有点没成果啊. 于是我打开了dify的api, 多少也弄个对话bot, 不然感觉好像忙活好久但是没什么阶段性的成果...

然后问题来了, cloud.dify.ai里的api没有写是啥语言, 然后python又似乎不是他们的偏好语言, 参考了下[Dify接入微信](https://docs.dify.ai/v/zh-hans/learn-more/use-cases/dify-on-wechat), 但Dify on WeChat和ChatGPT on WeChat有点技术栈对我这样一个CS新手来说过于沉重了, 加上我倾向于兼容yihong0618的库.

我又向上溯源, 再次感谢[pypi](https://pypi.org/project/dify-client/), 我通过这个资源的README和源代码的阅读, 总算是差不多了.

然后我简单地写了个`dify.py`(but it do take a bit long time there), 在手动输入配置Dify的app api到`.env`之后, 基本上一次就顺利运行了.

## 5.5

我注意到dify的是支持user和conversation_id的, 这可能更有益于节省token啥的, 所以我对handlers里的进行了一点修改, 加了个`c` stand for conversation_id, 以及用了个新的词典`dify_player_c = {}`来存储conversation_id和user_id.

总之是初步跑起来了, 感谢Yihong0618, Dify, Pypi, pyTelegramBotAPI, 以及python-telegram-bot!

---

To ChatGPT:
请你帮我细致地检查, 我是否可能冒犯到任何人?  (日记可能包含了一些吐槽和问题的提出)

---

在你的记录中，总体上你是在描述你在项目开发过程中的个人经历和一些技术挑战，而没有对任何个人或组织进行负面评论或攻击。以下是几个细节上的注意点：

1. **对工具的使用描述**：你提到了多个开源库和工具，如 `python-telegram-bot`, `pyTelegramBotAPI`, `Dify` 等，并且是在讨论它们在项目中的应用和功能，这些描述都是客观的。

2. **个人感受的表达**：你的文字中包含了一些关于感受疲惫、对技术挑战的吐槽，这是非常常见的个人日记或记录的一部分。这些表达并没有涉及到对任何第三方的负面评价，而是反映了你个人的体验和情感。

3. **技术问题的提出**：你提到了在学习过程中遇到的困难，比如API的语言不清楚、技术栈的复杂性等，这些都是在描述你个人的学习过程和挑战，而非批评。

4. **提及第三方资源和链接**：你在记录中提供了一些有用的资源链接，这可以看作是对这些资源的推荐，而非不当的使用。

因此，从这段记录来看，你的表述应该不会冒犯到任何人。它主要集中在个人的学习过程、使用的工具、以及遇到的挑战上，且语气主要是说明和叙述，没有侮辱或贬低任何人或组织的内容。如果你担心特定的部分可能会被误解，可以考虑稍微调整措词以确保表达的尊重和客观性。

---

Done. 2024-05-14 23:44:00
