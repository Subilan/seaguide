---
description: 「基本语法」指的是在本文的查看过程中，一些示例的格式规定，比如「指令」等。若您仍然无法理解「语法」的具体含义，请继续向下理解。
---

# 基本语法

> 本文可能含有大量**需要花费阅读时间**来进行阅读的项目，若您希望获取您所需要的讯息，建议直接在左栏中选择。

### 01 格式语法

我们的格式语法分为：

H1 章节标题 ＞ H2 块标题 ＞ H3 条目标题，其中可能含有 Blockquote 注释。

相信对于这些，您一定理解什么叫做「语法」了。在本文中，所有的格式都会遵从以上语法，才可让本文更加简洁明了且清晰。

### 02 指令语法

「指令语法」与「格式语法」并不是同一样东西。指令语法指的是在「指令」章节中我们所使用的，叙述指令的相关语法格式。在本文中，我们通常使用的指令语法有 2 种。

#### 02-01 普通语法

```text
/指令内容 <必填参数> [可选参数]
```

以上语法中表示得很清楚，指令内容就是我们所使用的指令的内容。比如 `/tpa` 就是一个独立的指令内容，后面不跟任何东西。然而如果您确实想要去 TPA 一个玩家，那么您就必须跟上他的玩家名，这样一来，「玩家名」便是必填参数，如果没有「必填参数」，那么就会导致指令直接执行失败。

因此，通过上面的解析，我们可以简单地写出 `/tpa` 指令的基本语法格式了：

```text
/tpa <玩家名>
```

#### 02-02 派生语法

> 此条目内容可能不会在\*\*玩家所玩内容\*\*中涉及，也就是说，如果您是普通玩家，则您无需深刻了解此部分内容。
>
>  此条目内容需要以下插件：LuckPerms for SpongAPI 8.1.0, Nucleus

派生语法指在一个原有指令的基础上，按照前面的部分指定的对象格式，加上后方的「操作」部分，从而达到对同一对象不同操作的指令组。

我们借用 LuckPerms 插件内的权限组设定来举一个例子：

```text
/lp group default
> ... permission set nucleus.vanish.onlogin true
> ... parent set players
```

这便是一个简单的指令组，其中，`/lp group default` 被称为「主指令」，以`> ...` 开头的指令被称为「派生指令」。派生指令的所有操作都是建立在其绑定的主指令基础上的。  
比如若主指令指定为`/lp group default` ，则此指令下所有派生指令的对象类型便都被指定为`group` 且对象的名称都被指定为`default` ，即`group.default` 。  
这样一来，派生指令的所有执行都是对 `group.default` 起作用的。

