[#]: collector: (lujun9972)
[#]: translator: (geekpi)
[#]: reviewer: ( )
[#]: publisher: ( )
[#]: url: ( )
[#]: subject: (Build a private chat server with a Raspberry Pi and Rocket.Chat)
[#]: via: (https://opensource.com/article/20/3/raspberry-pi-rocketchat)
[#]: author: (Giuseppe Cassibba https://opensource.com/users/peppe8o)

使用树莓派和 Rocket.Chat 构建一个私人聊天服务器
======
使用这些简单、经济高效的开源工具创建你自己的真正私人聊天和消息解决方案。
![Chat via email][1]

互联网提供大量免费的消息服务。WhatsApp 和 Viber 等应用是我们日常生活的一部分，也是我们与亲朋好友沟通的最常见方式。但是，安全意识正在增加对真正私人聊天解决方案的需求。此外，消息应用在我们的设备中占用了大量空间，因此备用聊天渠道可用于与朋友共享媒体、信息和联系人。

今天，我们将了解如何使用[树莓派][2]和 Rocket.Chat 安装一个私人聊天和消息服务器。

### 什么是 Rocket.Chat？

[Rocket.Chat][3] 是一个开源解决方案，它提供增强的聊天服务。它包括媒体共享、屏幕共享和视频/音频呼叫支持等协作工具。

它可以通过浏览器或从所有主要应用商店（Google Play、App Store 等）下载使用。

除了社区版本外，Rocket.Chat 还提供企业版和专业版，包括支持和其他功能。

### 我们需要什么

对于这个项目，我将使用更便宜的树莓派 3 model A+。树莓派 3 model B 和 B+ 以及树莓派 4 model B 工作应该一样。

我也建议使用高性能 SD 卡，因为 Rocket.Chat 会给树莓派大量的负载。如其他文章中所述，高性能 SD 卡可显著提高 Raspbian 操作系统的性能。

我们将使用 Raspbian 的精简版本，拥有预配置的 WiFi 访问和 SSH 服务，因此不需要键盘或 HDMI 线缆。

### 分步过程

从[安装最新版本的 Raspbian Buster Lite][5] 开始

我们将使用 [Snap][6] 简化 Rocket.Chat 安装。通过 SSH 登录并从终端输入：


```
sudo apt-get update
sudo apt-get upgrade
```

安装 Snap：


```
`sudo apt-get install snapd`
```

安装 Snap 后，我们需要重启系统使其正常工作：


```
`sudo reboot`
```

再次通过 SSH 登录，并用以下简单的命令安装 Rocket.Chat：


```
`sudo snap install rocketchat-server`
```

从终端安装后，请等待一段时间，等待 Rocket.Chat 初始化数据库和服务。休息一下，几分钟后，你应该能够在浏览器中访问 http://&lt;&lt;YOUR_RPI_IP_ADDRESS&gt;&gt;:3000，你应该看到以下内容：

![Rocket Chat setup wizard][7]

填写所需的表格就可以了。四个简单的设置窗口后，你应该会进入 Rocket.Chat 主页：

![Rocket Chat home page][8]

享受吧！

_本文最初发表在 [peppe8o.com][9]，并或许重新发布。_

--------------------------------------------------------------------------------

via: https://opensource.com/article/20/3/raspberry-pi-rocketchat

作者：[Giuseppe Cassibba][a]
选题：[lujun9972][b]
译者：[geekpi](https://github.com/geekpi)
校对：[校对者ID](https://github.com/校对者ID)

本文由 [LCTT](https://github.com/LCTT/TranslateProject) 原创编译，[Linux中国](https://linux.cn/) 荣誉推出

[a]: https://opensource.com/users/peppe8o
[b]: https://github.com/lujun9972
[1]: https://opensource.com/sites/default/files/styles/image-full-size/public/lead-images/email_chat_communication_message.png?itok=LKjiLnQu (Chat via email)
[2]: https://opensource.com/resources/raspberry-pi
[3]: https://rocket.chat/
[5]: https://peppe8o.com/2019/07/install-raspbian-buster-lite-in-your-raspberry-pi/
[6]: https://snapcraft.io/
[7]: https://opensource.com/sites/default/files/uploads/rocket-chat-setup-wizard.jpg (Rocket Chat setup wizard)
[8]: https://opensource.com/sites/default/files/uploads/rocket-chat-home.jpg (Rocket Chat home page)
[9]: https://peppe8o.com/private-chat-and-messaging-server-with-raspberry-pi-and-rocket-chat/