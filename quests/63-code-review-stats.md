IV - [系列任务 1 of 3]

小明有一天在翻代码库的时候，发现不知不觉间，M 站 (mobile-v3 项目) 的 Merge Request 数量已经超过 1000 了！小明想看一下，其中有多少是 code review 类型的。

所谓的 code review 类型，应该满足以下条件：

1. 不是小河狸机器人创建的
2. MR 应该被指派给了某个人，并且这个人不等于 MR 的创建人

小明知道 Gitlab 提供了 API 可以查询 MR，这个工具应该能够实现。正好最近在学习 Elixir, 不如就用 Elixir 来写一个命令行工具。这个工具可以这样用：

```console
# 打印帮助:
crstats --help

# 显示数据统计:
crstats show --host <HOST> --repo <REPO> 
# 如:
crstats show --host my.gitlab.com --repo web/mobile

code review stats of `web/mobile` on host `my.gitlab.com`
total: 1023
```

嗯，第一步这样应该就够了，以后可以慢慢在这个基础核心上包装新的功能。再复杂的功能也是这样简单的核心开始的。

#### 任务：

* 用 Elixir 开发统计 code review 统计的一个命令行工具。


#### 技能：

* Elixir
