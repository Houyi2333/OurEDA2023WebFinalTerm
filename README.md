# OurEDA 实验室 2023 级 Web 方向小学期作业

22-ly

## 前言

感谢您继续选择 Web 作为您的学习方向，在您完成本次作业之前请务必仔细阅读本文档以免您提交的内容与实际要求有所出入

从本次作业开始我们将进入后端开发的学习。后端开发是指在服务器端进行编程的工作，主要负责处理用户的请求，与数据库交互，实现业务逻辑，提供数据接口等。在后端的学习过程中，我们不会指定大家使用特定的编程语言、后端框架、数据库及其他中间件，但是在答辩的过程中各位同学应当体现自己对于自己所选用的技术栈的理解能力。目前各位对 JavaScript 比较熟悉，不妨学习例如 Express.js 等基于 Node.js 的后端框架[^1]

关于什么是后端开发，以及后端开发的具体技术路线应该如何规划，后端开发相关学习文档，当前后端开发有何前沿趋势，各位同学不妨参照以下资料：

* [后端开发技术路线 (Github 200k stars 开源项目)](https://roadmap.sh/backend)
* [闯关式 SQL 自学教程网站，从 0 到 1 带大家掌握常用 SQL 语法](https://github.com/liyupi/sql-mother)
* [图解网络 | 小林coding (生动易懂的计网文档)](https://xiaolincoding.com/network/)
* [Internet 是如何工作的 (计网必学内容)](https://cs.fyi/guide/how-does-internet-work)
* [Apifox 使用教程合集，从小白到大师](https://apifox.com/blog/apifox-tutorial-collection/)
* [StackOverflow 2023 年开发者调查报告 (重点需要关注 Technology 版块)](https://survey.stackoverflow.co/2023/)
* [TIOBE 编程语言排行榜 (看个乐子就行)](https://www.tiobe.com/tiobe-index/)

作业允许使用 AI 大模型辅助完成[^2]。但严格禁止各位同学抄袭互联网上的整个项目，严格禁止互相抄袭，一经发现取消答辩资格

## 作业需求

本次作业要求您重构您的[简易版 Todo List](https://github.com/Houyi2333/OurEDA2023WebMidTerm)，确保 GitHub 仓库只上传了必要的文件和目录，合理编写了 `README.md`；有良好的文件夹结构设计，健康的代码缩进风格，清晰的变量与类型命名风格；确保组件满足单一职责原则，且将具有独立功能模块的组件写在不同文件中；**迁移状态逻辑至 Reducer 中；在本地或云运行后端服务器，连接数据库实现数据持久化**[^3]

同时，您需要为您的简易版 Todo List 实现简易[^4]的登录注册系统，允许不同的用户创建不同的 Todo List

登录注册系统是最为基础也是最为常见的一套后端系统，但是麻雀虽小五脏俱全，一套完备的登录注册系统不仅包含了后端服务器最为常见的一组 CRUD 操作，更需要考验一位后端开发者的综合开发基本功

我们希望各位的登录注册系统在业务逻辑层面主要包含以下三个模块:

1. Login 模块
2. Logout 模块
3. Register 模块 (不是寄存器)

您的项目在水平层面应该有至少以下三个层次：

1. 前端
2. 后端
3. 数据库

## 准备答辩

#### 答辩 PPT

请使用 OurEDA 实验室官方提供的模板进行 PPT 制作，否则我们有权取消您的答辩资格

我们希望您的 PPT 中包含以下内容：

1. 大一下学期与 Web 相关的学习内容总结
2. 项目总结
3. 新学期的个人规划与展望

我们不希望您的 PPT 中包含以下内容：

1. 对源代码的大段复制粘贴或截图
2. 与项目无关的其他内容

#### 答辩流程

1. PPT 放映
2. 提问

*注：提问内容包括但不仅限于 Todo List 项目本身*

## 可选项

本项若在小学期未完成，将作为您暑假作业的一部分

在实际的 Web 项目中，登录注册系统并不是简单的校验账号密码是否正确，包括但不仅限于以下几种常见的方法：

1. 基于 Session 的认证
2. 基于 Token 的认证
3. 多因素验证（如短信验证码、电子邮件验证码、生物识别或硬件令牌）
4. SSO 单点登录

目前最常用的登录注册系统实现方法是基于 Token 的身份验证机制，特别是使用 JSON Web Tokens（JWT）。这种方法因其简单性、无状态性、可扩展性以及适用于分布式系统的特点而广受欢迎。JWT 允许在客户端和服务器之间安全地传递用户认证信息，而不需要在服务器上存储 Session 状态。此外，Token 认证机制还支持跨域认证，使其非常适合现代的微服务架构和移动应用。用户发出登录请求，带着用户名和密码到服务器经行验证，服务器验证成功就在后台生成一个 Token 返回给客户端，后续客户端的每次请求资源都必须携带 Token。具体流程可参考 [基于Token的登录流程](https://cloud.tencent.com/developer/article/1444727)

[^1]:你说得对， 但是《Golang》是由 Google 公司自主研发的一款全新开放世界编程语言。语言发生在一个被称作「现代编程」的数字化世界，在这里，被开发者选中的代码将被授予「高效执行」，导引并发之力。你将扮演一位名为「开发者」的神秘角色，在自由的旅行中邂逅功能强大、易于使用的框架们，和它们一起解决难题，实现产品的需求——同时，逐步发掘「Golang」的真相
[^2]:答辩时我们会对疑似 AI 生成的部分进行提问
[^3]:该要求指您需要将 Todo List 保存在数据库中以实现项目重启后可以保留上次状态
[^4]:“简易”一词指允许通过简单的校验账号密码是否正确实现登录注册，但不允许将用户名和密码以明文的形式存储在数据库中，不要求实现基于 Session 的认证、基于 Token 的认证等方法
