# API

### Telegram APIs

我们为开发者提供了两种类型的 API。[**Bot API**](https://core.telegram.org/#bot-api) 允许你轻松创建使用 Telegram 消息作为界面的程序。 [**Telegram API 和 TDLib**](https://core.telegram.org/#tdlib--build-your-own-telegram) 让你能够构建自己定制的 Telegram 客户端。欢迎您免费的使用这两种 API。

您也可以在您的网站上添加 [**Telegram 小部件**](https://core.telegram.org/widgets)。

我们欢迎设计师为 Telegram 创建[**动画贴纸**](https://core.telegram.org/animated_stickers)或[**自定义主题**](https://core.telegram.org/themes)。

------

### Bot API

这个 API 允许你将机器人连接到我们的系统。[**Telegram 机器人**](https://core.telegram.org/bots)是特殊的账户，不需要设置额外的电话号码。这些账户作为在你服务器上某处运行的代码的接口。

使用这个 API，你不需要了解我们的 MTProto 加密协议是如何工作的——我们的中间服务器将为你处理所有加密和与 Telegram API 的通信。你通过一个简单的HTTPS接口与这个服务器进行通信，该接口提供了 Telegram API 的简化版本。

>   [**在此处了解有关 Bot API 的更多信息 »**](https://core.telegram.org/bots)

机器人开发者还可以利用我们的 [**Payments API**](https://core.telegram.org/bots/payments) 接受来全世界各地的 Telegram 用户**付款。**

------

### TDLib – 构建您自己的 Telegram

即使您寻求最大程度的定制，也无需从头开始创建你的应用程序。尝试使用我们的 [**Telegram 数据库库**](https://core.telegram.org/tdlib)（或简称 TDLib），这是一个供第三方开发者使用的工具，它可让您轻松构建快速、安全且功能丰富的 Telegram 应用程序。

TDLib 负责所有**网络实现**细节、**加密**和**本地数据存储**，因此你可以将更多时间用于设计、响应式界面和美观的动画上。

TDLib 支持所有的 Telegram 功能，并使在任何平台上开发 Telegram 应用变得轻而易举。它可以在 Android、iOS、Windows、macOS、Linux 和几乎任何其他系统上使用。该库是开源的，并且几乎与**任何编程语言**兼容。

>   [**在此处了解有关 TDLib 的更多信息 »**](https://core.telegram.org/tdlib)

------

### Telegram API

该 API 允许您构建自己定制的 Telegram 客户端。它对所有希望在我们的平台上创建 Telegram 应用程序的开发者 100% 开放。欢迎自由研究现有的 Telegram 应用程序的[开源代码](https://telegram.org/apps#source-code)，以获取有关此处工作原理的示例。不要忘记在我们的系统中[注册](https://core.telegram.org/api/obtaining_api_id)您的应用程序。

-   [入门](https://core.telegram.org/#getting-started)
-   [安全性](https://core.telegram.org/#security)
-   [优化](https://core.telegram.org/#optimization)
-   [API方法](https://core.telegram.org/#api-methods)

### 入门

#### [创建一个应用程序](https://core.telegram.org/api/obtaining_api_id)

如何获取您的应用程序标识符并创建一个新的 Telegram 应用程序。

#### [用户授权](https://core.telegram.org/api/auth)

如何注册用户的电话以开始使用 API。

#### [两步验证](https://core.telegram.org/api/srp)

如果启用了 2FA，如何登录用户帐户，如何更改密码。

#### [二维码登录](https://core.telegram.org/api/qr-login)

[二维码](https://en.wikipedia.org/wiki/QR_code)登录流程

#### [错误处理](https://core.telegram.org/api/errors)

如何正确处理 API 返回错误。

#### [处理不同的数据中心](https://core.telegram.org/api/datacenter)

如何连接到最近的 DC 接入点以更快地与 API 交互，以及开发客户端时需要注意的事项。

#### [处理更新](https://core.telegram.org/api/updates)

如何订阅更新并正确处理它们。

#### [处理 PUSH 推送通知](https://core.telegram.org/api/push-updates)

如何订阅并正确处理它们。

#### [频道、超级群组、巨型群组和基本群组](https://core.telegram.org/api/channel)

如何处理频道、超级群组、巨型群组、基本群组，以及它们之间的区别。

#### [论坛](https://core.telegram.org/api/forum)

Telegram 允许创建具有多个不同主题的论坛。

#### [频道统计](https://core.telegram.org/api/stats)

Telegram 为频道和超级群组提供详细的频道统计信息。

#### [调用方法](https://core.telegram.org/api/invoking)

调用方法的额外选项。

#### [上传和下载文件](https://core.telegram.org/api/files)

如何正确传输大批量数据。

#### [分页](https://core.telegram.org/api/offsets)

如何从大量对象列表中获取结果。

#### [客户端配置](https://core.telegram.org/api/config)

MTProto API 具有多个客户端配置参数，可以用相应的方法获取。

### 安全性

#### [秘密聊天、端到端加密](https://core.telegram.org/api/end-to-end)

端到端加密消息传递。

#### [安全指南](https://core.telegram.org/mtproto/security_guidelines)

你的客户端应用程序中所需的重要检查。

#### [完美的前向保密](https://core.telegram.org/api/pfs)

将临时授权密钥与永久授权密钥绑定。

#### [端到端加密的语音和视频通话](https://core.telegram.org/api/end-to-end/video-calls)

端到端加密通话。

### 优化

#### [客户端优化](https://core.telegram.org/api/optimisation)

提升 API 交互的方法。

### API 方法

#### [可用方法列表](https://core.telegram.org/methods)

可用的高级方法列表。

#### [API TL-schema](https://core.telegram.org/schema)，[以 JSON 格式](https://core.telegram.org/schema/json)

在 API 中使用的类型和方法的文本和 JSON 表示。

#### [可用图层列表](https://core.telegram.org/api/layers)

可用的架构版本列表。

### 其他文章

#### [使用 MTProto API 处理机器人](https://core.telegram.org/api/bots)

如何使用 MTProto API 与机器人交互。

#### [命令](https://core.telegram.org/api/bots/commands)

[机器人](https://core.telegram.org/bots)提供一组命令，用户可以在私聊中或在聊天中使用。

#### [按钮](https://core.telegram.org/api/bots/buttons)

用户可以通过**按钮**或甚至是聊天中**任何消息**的**内联按钮**与你的机器人进行互动。

#### [菜单按钮](https://core.telegram.org/api/bots/menu)

机器人可以选择显示在文本输入字段旁边的菜单按钮的行为。

#### [内联查询](https://core.telegram.org/api/bots/inline)

用户可以通过内联查询与你的机器人互动，直接从**任何**聊天的**文本输入字段**中。

#### [游戏](https://core.telegram.org/api/bots/games)

机器人可以为用户提供 HTML5 游戏，供用户单独玩或在群组和一对一聊天中与其他用户竞争；如何在MTProto API中处理游戏。

#### [迷你应用程序](https://core.telegram.org/api/bots/webapps)

机器人可以为用户提供交互式[HTML5 迷你应用程序](https://core.telegram.org/bots/webapps)，以完全替代**任何网站**。

#### [附件菜单](https://core.telegram.org/api/bots/attach)

机器人可以安装附件菜单条目，提供方便可访问、多功能的迷你应用程序。

#### [故事](https://core.telegram.org/api/stories)

Telegram 用户和频道可以通过 API轻松发布和查看[故事](https://telegram.org/blog/stories)。

#### [相似频道](https://core.telegram.org/api/recommend)

API提供一种方法，根据其**订阅者**基础的相似性，获取一系列主题相似的公开频道。

#### [强调色](https://core.telegram.org/api/colors)

Telegram 用户和频道可以更改他们的个人资料页面以及他们的消息的强调色和背景图案！

#### [隐私设置](https://core.telegram.org/api/privacy)

Telegram 允许用户指定细粒度的隐私设置，选择哪些用户可以或不能以某种方式与他们互动。

#### [搜索和过滤器](https://core.telegram.org/api/search)

Telegram 允许在聊天中查找消息时应用详细的消息过滤器。这允许服务器根据文本查询和消息类型过滤消息，这个功能经常被图形客户端用来实现诸如聊天画廊、聊天资料图片等功能。

#### [投票](https://core.telegram.org/api/poll)

Telegram 允许发送投票和测验，可以由数千甚至数百万的用户在聊天和频道中进行投票。

#### [回应](https://core.telegram.org/api/reactions)

Telegram 允许用户使用特定的表情符号对任何消息进行回应，触发可爱的 lottie 动画。

#### [表情状态](https://core.telegram.org/api/emoji-status)

[Telegram 允许用户设置一个表情符号或自定义表情符号](https://core.telegram.org/api/custom-emoji)作为状态，以显示在聊天和个人资料中的姓名旁边。

#### [邀请链接和加入请求](https://core.telegram.org/api/invites)

频道、基本群组和超级群组可以有一个公共用户名或一个私人邀请链接：私人邀请链接可以进一步增强，增加每个用户的加入请求。

#### [频道、超级群组和群组的管理员、禁止和默认权限](https://core.telegram.org/api/rights)

如何处理频道、群组和超级群组的管理员权限、细化禁止和全局权限。

#### [讨论组](https://core.telegram.org/api/discussion)

[群组](https://core.telegram.org/api/channel)可以作为[讨论组与](https://telegram.org/blog/privacy-discussions-web-bots)[频道](https://core.telegram.org/api/channel)关联，以便用户讨论帖子内容。

#### [频道评论和消息线程](https://core.telegram.org/api/threads)

由于消息线程，Telegram允许在[频道帖子](https://core.telegram.org/api/channel)或[普通群组消息上发表评论](https://core.telegram.org/api/channel)。

#### [管理员日志](https://core.telegram.org/api/recent-actions)

超级群组和频道都提供所谓的[管理员日志](https://telegram.org/blog/admin-revolution)，记录最近的相关超级群组和频道动作，例如代表管理员修改群组/频道设置或信息、用户踢出和禁令等。

#### [置顶消息](https://core.telegram.org/api/pin)

Telegram允许在特定聊天顶部之上置顶多条消息。

#### [提及](https://core.telegram.org/api/mentions)

Telegram 允许在出现紧急问题时提及其他用户，并快速导航到这些提及的内容以便尽快阅读它们。

#### [定时消息](https://core.telegram.org/api/scheduled-messages)

Telegram 允许定时发送消息。

#### [实时地理位置](https://core.telegram.org/api/live-location)

Telegram 允许在聊天中发送用户的实时地理位置，可以选择设置接近警报。

#### [最小构造函数](https://core.telegram.org/api/min)

有时，在群聊更新中遇到的[用户](https://core.telegram.org/constructor/user)和[频道](https://core.telegram.org/constructor/channel)构造函数可能不包含有关用户的完整信息：如何处理此类构造函数。

#### [帐户删除](https://core.telegram.org/api/account-deletion)

如何删除 Telegram 帐户。

#### [导入的消息](https://core.telegram.org/api/import)

Telegram 允许从外部聊天应用程序导入消息和媒体。

#### [Telegram 护照](https://core.telegram.org/api/passport)

如何直接使用 MTProto API 操作 [Telegram Passport](https://core.telegram.org/api/passport)。

#### [Telegram 支付](https://core.telegram.org/api/payments)

如何直接使用 MTProto API 处理 Telegram 支付。

#### [带有消息实体的样式文本](https://core.telegram.org/api/entities)

如何创建带有消息实体的样式文本

#### [使用贴纸](https://core.telegram.org/api/stickers)

Telegram 客户端支持显示动画、静态和视频贴纸。

#### [使用自定义表情符号](https://core.telegram.org/api/custom-emoji)

Telegram 允许直接在消息中包含自定义动画、静态和视频表情符号。

#### [使用动画表情符号](https://core.telegram.org/api/animated-emojis)

图形 Telegram 客户端应将表情符号转换为各自的动画版本。

#### [使用动画骰子](https://core.telegram.org/api/dice)

Telegram 支持发送[动画骰子](https://telegram.org/blog/folders#and-one-more-thing)表情符号。

#### [消息草稿](https://core.telegram.org/api/drafts)

如何处理消息草稿。

#### [文件夹](https://core.telegram.org/api/folders)

处理文件夹。

#### [顶级对等评级](https://core.telegram.org/api/top-rating)

如果[启用](https://core.telegram.org/method/contacts.toggleTopPeers)，[顶级对等体](https://core.telegram.org/constructor/topPeer)的评级表示特定[类别](https://core.telegram.org/type/TopPeerCategory)中（频繁消息的用户、频繁使用的机器人、内联机器人、频繁访问的频道等）的相关性。

#### [使用文件引用](https://core.telegram.org/api/file_reference)

如何使用文件引用。

#### [无缝 Telegram 登录](https://core.telegram.org/api/url-authorization)

处理无缝 Telegram 登录 URL 授权请求。

#### [壁纸](https://core.telegram.org/api/wallpapers)

如何使用聊天背景。

#### [通知声音](https://core.telegram.org/api/ringtones)

如何使用聊天通知声音。

#### [消息转录](https://core.telegram.org/api/transcribe)

如何转录语音消息。

#### [消息翻译](https://core.telegram.org/api/translation)

Telegram 允许翻译聊天消息，[Telegram Premium](https://core.telegram.org/api/premium)用户甚至可以启用实时聊天翻译。

#### [原生反垃圾邮件系统](https://core.telegram.org/api/antispam)

拥有一定数量成员的超级组的管理员可以选择充分发挥 Telegram 自己的反垃圾邮件算法的全面主动力量 - 为自动垃圾邮件过滤器打开新的 Aggressive (积极) 模式。

#### [可收集的用户名](https://core.telegram.org/api/fragment)

Telegram 用户可以通过[用户名](https://telegram.org/faq#usernames-and-t-me)轻松让其他人联系他们或找到他们的公开群组和频道：客户端还可以为他们拥有的帐户、超级群组和频道分配多个Telegram 用户可以通过用户名轻松让其他人联系他们或找到他们的公开群组和频道：客户端还可以为他们拥有的帐户、超级群组和频道分配多个可收集的用户名。

#### [频道提升](https://core.telegram.org/api/premium)

[Telegram Premium](https://core.telegram.org/api/premium) 用户可以通过给他们最喜欢的频道提供额外的功能，例如通过给予他们**支持来发布**[故事的](https://core.telegram.org/api/stories)能力。

#### [赠品和礼物](https://core.telegram.org/api/giveaways)

Telegram[频道](https://core.telegram.org/api/channel)管理员可能会推出赠品活动，通过在其关注者中随机分发[Telegram Premium](https://core.telegram.org/api/premium)订阅和其他礼物，以换取[奖励](https://core.telegram.org/api/boost)。

#### [操作栏](https://core.telegram.org/api/action-bar)

有时，当通过私人或秘密聊天与 Telegram 用户交互时，必须在聊天顶部显示操作栏，提供便捷的操作按钮或有关用户的通知。

#### [已保存的消息](https://core.telegram.org/api/saved-messages)

“保存的消息”聊天允许用户为消息和媒体添加书签：这是一个个人云存储，用于存储您可能想要发送或转发的任何消息或媒体。。

### [联系人](https://core.telegram.org/api/contacts)

在 API 中处理联系人。

### [黑名单](https://core.telegram.org/api/block)

处理黑名单。

### [附近的用户&聊天](https://core.telegram.org/api/nearby)

如何使用基于地理位置的功能，例如地理聊天和附近的用户功能。

#### [网页事件](https://core.telegram.org/api/web-events)

与 HTML5 游戏和支付网关网站互动时，Telegram 应用应公开以下 JS API。

#### [导出](https://core.telegram.org/api/takeout)

Telegram 的 API 允许用户通过 takeout API 导出他们的所有信息。