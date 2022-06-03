# 介绍与安装

## 介绍与安装

停止使用只有一些令人困惑的功能的旧框架吧！ Masonite 是专注于开发人员的开发工具，具有你应得的快速开发所需的所有功能。 Masonite 非常适合部署第一个 Web 应用程序的初学者或需要使用全部可用功能的高级开发人员和企业。

Masonite 努力实现从安装到部署的快速和简单，因此开发人员可以尽可能快速高效地从概念到创建。将它用于你的下一个 SaaS！尝试一次，你就会爱上它。

{% hint style="success" %}
提示：如果你更喜欢通过视觉进行学习，可以在 [MasoniteCasts.com](https://masonitecasts.com) 观看 Masonite 相关教程视频。
{% endhint %}

### Masonite 附带的一些特色功能

* 邮件支持：快速发送电子邮件。
* 队列支持通过发送作业在队列上或异步运行来加速你的应用程序。
* 通知服务支持简单有效地向你的用户发送通知。
* 任务计划按计划运行你的工作（例如每天午夜），这样你就可以设置和忘记你的任务。
* 当你的应用程序中发生某些事件时，你可以侦听以执行执行任务的侦听器的事件。
* 一个漂亮的 Active Record 风格的 ORM，称为 Masonite ORM。这是你触手可及的惊喜。
* 你可以在文档中找到更多你需要的功能！

除了许多其他功能外，这些功能都已开箱即用。在需要时使用你需要的东西。

### 要求

为了使用 Masonite，你需要：

* Python 3.7+
* 最新版本的 OpenSSL
* Pip3

{% hint style="warning" %}
注意：本文档中的所有 python 和 pip 命令都假设它们指向正确的 Python 3 版本。例如，在任何你看到 `python` 命令运行的地方，它都假定是 Python 3.7 Python 安装。如果你在任何安装步骤中遇到问题，请确保这些命令适用于 Python 3.7 而不是 2.7 或更低版本。
{% endhint %}

#### Linux

如果你在 Linux 上运行，你需要 Python dev 包和 libssl 包。你可以通过运行下载这些包：

#### **Debian and Ubuntu based Linux distributions**

{% code title="terminal" %}
```
$ sudo apt install python3-dev python3-pip libssl-dev build-essential python3-venv
```
{% endcode %}

或者你可能需要指定你的 `python3.x-dev` 版本：

{% code title="terminal" %}
```
$ sudo apt-get install python3.7-dev python3-pip libssl-dev build-essential python3-venv
```
{% endcode %}

基于企业 Linux 的发行版（Fedora、CentOS、RHEL、...）

{% code title="terminal" %}
```
# dnf install python-devel openssl-devel
```
{% endcode %}

### 安装

{% hint style="success" %}
提示：请务必加入 [Discord 社区](https://slack.masoniteproject.com) 以获得帮助或指导。
{% endhint %}

Masonite 擅长安装和使用简单。如果你来自以前版本的 Masonite，则某些安装步骤的顺序会发生一些变化。

首先，打开一个终端并前往你要在其中创建应用程序的目录。你可能希望在编程目录中创建它，例如：

```
$ cd ~/programming
$ mkdir myapp
$ cd myapp
```

如果你在 Windows 上，你可以创建一个目录并在 Powershell 中打开该目录。

### 激活虚拟环境（可选）

尽管此步骤在技术上是可选的，但强烈建议这样做。如果你不想在系统 Python 上安装所有 masonite 的依赖项，则可以创建一个虚拟环境。如果您使用虚拟环境，则通过运行以下命令创建您的虚拟环境：

{% code title="terminal" %}
```
$ python -m venv venv
$ source venv/bin/activate
```
{% endcode %}

或者如果你使用的是 Windows：

{% code title="terminal" %}
```
$ python -m venv venv
$ ./venv/Scripts/activate
```
{% endcode %}

{% hint style="info" %}
提示：此处的 `python` 命令使用 Python 3。对于 UNIX 机器，你的机器可能默认运行 Python 2 （通常为 2.7）。你可以在你的机器上为 Python 3 设置一个别名，或者只要你看到 `python` 命令，就直接运行 `python3`。
{% endhint %}

## 安装 Masonite 包

首先安装 Masonite 包：

```
$ pip install masonite
```

然后开始一个新项目：

```
$ project start .
```

这将在当前目录中创建一个新项目。

{% hint style="info" %}
提示：如果你想在新目录中创建项目（例如 `my_project`），你必须提供目录名称和 `project start my_project。`
{% endhint %}

然后安装 Masonite 依赖项：

```
$ project install
```

{% hint style="info" %}
提示：如果你在新目录中创建了项目，则必须在运行 `project install` 之前进入该目录。
{% endhint %}

安装后，你可以运行开发服务器：

```
$ python craft serve
```

恭喜！你已经设置了你的第一个 Masonite 项目！继续了解有关如何使用 Masonite 构建应用程序的更多信息。
