# 重构与模式

## 写作缘由

### 过度设计

- 指代码的灵活性和复杂性超出所需

### 设计不足

- 指所开发的软件设计不良

### 测试驱动开发和持续重构

- 编程对话

  - 问：编写一个测试，想系统提问

    - 红

  - 答：编写代码通过这个测试，回答这一提问

    - 绿

  - 提炼： 通过合并概念、消除歧义，提炼你的回答

    - 重构

  - 反复： 提出下一个问题，继续进行对话

- 优点

  - 保持较低的缺陷数量
  - 大胆地进行重构
  - 得到更加简单、更加优秀的代码
  - 编程时没有压力

### 重构与模式

- 模式是重构的目的地
- 重构是抵达这个目的地的道路

### 演进式设计

- 学习了解优秀软件设计的演变过程比学习优秀设计本身更有价值
- 测试驱动开发和持续重构是演进式设计的关键实践

## 重构

### 何谓重构

- 重构

  - 保持行为的转换
  - 重构是一种对软件内部结构的改善，目的是在不改变软件的可见行为的情况下，使其更易理解，修改成本更低

- 重构过程

  - 去除重复、简化复杂逻辑和澄清模糊的代码

### 重构的动机

- 使新代码的增加更容易
- 改善既有代码的设计
- 对代码理解更透彻
- 提高编程的趣味性

### 众目睽睽

- 所有优秀的著述，都是不断修改而成的

  - 修改意味着重新审视

- 要得到最佳的重构结果，需要多人帮助

  - 极限编程采用结对编程和代码集体所有的原因之一

### 可读性好的代码

- 任何傻瓜都会编写计算机能理解的代码。好的程序员能够编写人能够理解的代码

### 保持清晰

- 保持代码清晰类似于保持房间清洁
- 方法

  - 持续地去除重复
  - 简化
  - 澄清代码
  - 不能容忍代码脏乱

### 循序渐进

- 采取更小、更安全的步骤比采取更大的步骤更能快速达到目标

### 设计欠账

- 指无法做如下三件事

  - 去除重复
  - 简化代码
  - 澄清代码的意图

- 向上沟通

  - 使用欠账这样的金融隐喻来讨论技术问题

### 演变出新的架构

- 应用需求驱动框架
- 通过重构，持续改进应用程序和框架

### 复合重构

- 由多个低层次重构组成的高层次重构

  - 所完成的许多工作都涉及代码的搬移

- 测试是复合重构不可分割的一部分

### 测试驱动的重构

- 应用测试驱动开发得到替换代码，然后将老代码替换为新代码

  - 同事保留并重新运行老代码的测试

- 应用场景

  - 替换算法

### 复合重构的优点

- 描述了重构顺序的完整计划

  - 更安全
  - 更有效
  - 更高效

- 能够提示不明显的设计方向

  - 复合重构引导你从源头走到目的地

- 促进对实现模式的深入思考

  - 思考模式的各种实现方案是大有收益的

## 模式

### 何谓模式

- 三部分组成的规则

  - 某一坏境、一个问题以及解决问题的方案之间的关系

### 模式痴迷

- 指某人对模式过于痴迷，以至于无法不在代码中使用模式

### 实现模式的方式不止一种

### 通过重构实现、趋向和去除模式

- 目的是获得更好的设计，而不是实现模式

### 模式是否会使代码更加复杂

- 人们对模式的熟悉程度对于他们如何看待基于模式的重构将起决定性作用

### 模式知识

- 读优秀的模式图书来学习
- 建立学习小组

## 代码坏味

### 常见的设计问题

- 重复
- 不清晰
- 复杂

### 十二种坏味道

- 重复代码

  - 形成 Template Method
  - 用 Factory Method 引入多态创建
  - 链构造函数
  - 用 Composite 替换一/多之分
  - 提取 Composite 
  - 通过 Adapter 统一接口
  - 引入 Null  Object

- 方法过长

  - 组合方法
  - 将聚集操作搬移到 Collecting Parameter
  - 用 Command 替换条件调度程序
  - 将聚集操作搬移到 Visitor
  - 用 Strategy 替换条件逻辑

- 条件逻辑太复杂

  - 用 Strategy 替换条件逻辑
  - 将修饰功能搬移到 Decorator
  - 用 State 替换状态改变条件语句
  - 引入 Null Object

- 基本类型迷恋

  - 用类替换类型代码
  - 用 State 替换状态改变条件语句
  - 用 Strategy 替换条件逻辑
  - 用 Composite 替换隐含树
  - 用 Interpreter 替换隐式语言
  - 将装饰功能搬移到 Decorator
  - 用 Builder 封装 Composite

- 冗赘类

  - 内联 Singleton

- 类过大

  - 用 Command 替换条件调度程度
  - 用 State 替换状态改变条件语句
  - 用 Interpreter 替换隐式语言

- 分支语句

  - 用 Command 替换条件调度程度
  - 将聚集操作搬移到 Visitor

- 组合爆炸

  - 用 interpreter 替换隐式语言

- 怪异解决方案

  - 通过 Adapter 统一接口

## 创建

### 用 Creation Method 替换构造函数
### 将创建知识搬移到 Factory
### 用 Factory 封装类
### 用 Factory Method 引入多态创建
### 用 Builder 封装 Composite
### 内联 Singleton 


## 简化

### 组合方法 Composed Method 