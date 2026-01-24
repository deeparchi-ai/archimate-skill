---
name: archimate
version: 1.0.0
description: ArchiMate 3.2 企业架构建模语言标准。提供完整的元素类型（战略层、业务层、应用层、技术层、物理层、实施迁移层、动机层）、关系类型、视角和视图定义。用于企业架构建模、架构文档化、架构分析和架构治理。
author: DeepArchi
license: MIT
keywords:
  - archimate
  - enterprise-architecture
  - modeling-language
  - architecture-framework
  - opengroup
  - togaf
---

# ArchiMate Skill - 企业架构建模语言

## 概述

ArchiMate 是 The Open Group 维护的企业架构建模语言标准。本技能提供 ArchiMate 3.2 规范的完整指导，包括所有元素类型、关系类型、视角定义和最佳实践。

## 何时使用

当用户需要：
- 了解 ArchiMate 建模语言规范
- 识别正确的 ArchiMate 元素类型
- 选择合适的关系类型连接元素
- 设计架构视角和视图
- 进行架构文档化
- 验证架构模型的合规性

## ArchiMate 核心框架

### 层次结构 (Layers)

```
┌─────────────────────────────────────────────────────────────────┐
│                      战略层 Strategy                             │
│  资源、能力、价值流、行动方案                                      │
├─────────────────────────────────────────────────────────────────┤
│                      业务层 Business                             │
│  参与者、角色、流程、服务、对象、事件、合同                         │
├─────────────────────────────────────────────────────────────────┤
│                      应用层 Application                          │
│  组件、接口、服务、数据对象、协作                                   │
├─────────────────────────────────────────────────────────────────┤
│                      技术层 Technology                           │
│  节点、设备、系统软件、网络、路径、通信                             │
├─────────────────────────────────────────────────────────────────┤
│                      物理层 Physical                             │
│  设施、设备、材料、分布网络                                        │
└─────────────────────────────────────────────────────────────────┘
```

### 方面维度 (Aspects)

| 方面 | 说明 | 元素类型 |
|------|------|----------|
| **主动结构 (Active)** | 执行行为的主体 | Actor, Role, Component, Node |
| **行为 (Behavior)** | 主体执行的活动 | Process, Service, Function |
| **被动结构 (Passive)** | 行为操作的对象 | Object, Data Object, Artifact |

## 元素类型详解

### 1. 战略层元素 (Strategy Layer)

| 元素 | 符号 | 说明 |
|------|------|------|
| Resource | 矩形+对角线 | 组织拥有或控制的资产 |
| Capability | 圆角矩形 | 组织的能力 |
| Value Stream | 箭头形 | 端到端的价值创造活动序列 |
| Course of Action | 圆角矩形+箭头 | 实现目标的行动方案 |

### 2. 业务层元素 (Business Layer)

**主动结构元素:**
| 元素 | 说明 |
|------|------|
| Business Actor | 能够执行行为的组织单元或个人 |
| Business Role | 业务参与者承担的职责 |
| Business Collaboration | 角色的临时配置以执行集体行为 |
| Business Interface | 业务服务的访问点 |

**行为元素:**
| 元素 | 说明 |
|------|------|
| Business Process | 基于事件顺序产生结果的行为 |
| Business Function | 基于资源分组的行为 |
| Business Interaction | 协作执行的行为 |
| Business Event | 触发或影响行为的事件 |
| Business Service | 对外暴露的业务行为 |

**被动结构元素:**
| 元素 | 说明 |
|------|------|
| Business Object | 业务领域的概念 |
| Contract | 参与者间的正式或非正式协议 |
| Representation | 业务对象的感知形式 |
| Product | 提供给客户的服务和被动结构的组合 |

### 3. 应用层元素 (Application Layer)

| 元素 | 说明 |
|------|------|
| Application Component | 封装应用功能的模块化单元 |
| Application Collaboration | 组件的临时配置 |
| Application Interface | 应用服务的访问点 |
| Application Function | 组件执行的自动化行为 |
| Application Interaction | 协作执行的自动化行为 |
| Application Process | 应用组件执行的自动化流程 |
| Application Event | 应用状态变化或输出 |
| Application Service | 对外暴露的应用行为 |
| Data Object | 用于自动处理的数据 |

### 4. 技术层元素 (Technology Layer)

| 元素 | 说明 |
|------|------|
| Node | 计算或物理资源 |
| Device | 物理计算资源 |
| System Software | 在节点上运行的软件环境 |
| Technology Collaboration | 节点的临时配置 |
| Technology Interface | 技术服务的访问点 |
| Path | 节点间的物理链接 |
| Communication Network | 物理或逻辑通信媒介 |
| Technology Function | 技术行为 |
| Technology Process | 技术流程 |
| Technology Interaction | 技术协作行为 |
| Technology Event | 技术事件 |
| Technology Service | 技术服务 |
| Artifact | 物理数据或软件 |

### 5. 物理层元素 (Physical Layer)

| 元素 | 说明 |
|------|------|
| Equipment | 物理机器或设备 |
| Facility | 物理场所 |
| Distribution Network | 物理分布网络 |
| Material | 有形物质 |

### 6. 实施与迁移层 (Implementation & Migration)

| 元素 | 说明 |
|------|------|
| Work Package | 可交付的工作单元 |
| Deliverable | 工作包的输出 |
| Implementation Event | 实施状态变化 |
| Plateau | 架构的相对稳定状态 |
| Gap | 两个状态间的差异 |

### 7. 动机层元素 (Motivation Layer)

| 元素 | 说明 |
|------|------|
| Stakeholder | 对架构有利益关系的人或组织 |
| Driver | 创建、约束或维持架构的外部条件 |
| Assessment | 对驱动因素的评估结果 |
| Goal | 想要达到的高层级状态 |
| Outcome | 期望达到的端到端结果 |
| Principle | 指导决策的规范性陈述 |
| Requirement | 必须实现的需求 |
| Constraint | 对实现的限制 |
| Meaning | 概念的知识或专业理解 |
| Value | 元素的相对价值 |

## 关系类型

### 结构关系 (Structural)

| 关系 | 符号 | 说明 | 示例 |
|------|------|------|------|
| Composition | 实心菱形 | 整体-部分，强生命周期 | 应用组件包含数据对象 |
| Aggregation | 空心菱形 | 整体-部分，弱生命周期 | 业务角色聚合业务参与者 |
| Assignment | 实心圆+线 | 分配资源执行行为 | 角色分配给流程 |
| Realization | 虚线空三角 | 抽象到具体实现 | 服务实现接口 |

### 依赖关系 (Dependency)

| 关系 | 符号 | 说明 | 示例 |
|------|------|------|------|
| Serving | 实线箭头 | 提供功能给另一元素 | 应用服务服务于业务流程 |
| Access | 虚线箭头 | 读取/写入被动结构 | 流程访问数据对象 |
| Influence | 虚线箭头(+/-) | 影响动机元素 | 驱动因素影响目标 |
| Association | 实线 | 通用关联 | 利益相关者关联目标 |

### 动态关系 (Dynamic)

| 关系 | 符号 | 说明 | 示例 |
|------|------|------|------|
| Triggering | 实线箭头 | 触发行为执行 | 事件触发流程 |
| Flow | 虚线箭头 | 传递内容 | 流程间数据流动 |

### 其他关系

| 关系 | 符号 | 说明 |
|------|------|------|
| Specialization | 空三角箭头 | 继承/特化 |
| Junction | AND/OR 节点 | 分支/合并 |

## 标准视角 (Viewpoints)

### 基础视角

| 视角 | 用途 | 主要元素 |
|------|------|----------|
| Organization | 展示组织结构 | Actor, Role, Location |
| Business Process Cooperation | 展示流程协作 | Process, Service, Role |
| Product | 展示产品组成 | Product, Service, Contract |
| Application Cooperation | 展示应用协作 | Component, Service, Interface |
| Application Usage | 展示应用使用 | Process, Component, Data |
| Infrastructure | 展示基础设施 | Node, Device, Network |
| Infrastructure Usage | 展示基础设施使用 | Component, Node, System Software |
| Layered | 展示层次结构 | 所有层元素 |

### 动机视角

| 视角 | 用途 |
|------|------|
| Stakeholder | 利益相关者及其关注点 |
| Goal Realization | 目标到实现的追溯 |
| Requirements Realization | 需求到实现的追溯 |
| Motivation | 完整动机结构 |

### 策略视角

| 视角 | 用途 |
|------|------|
| Strategy | 战略规划 |
| Capability Map | 能力地图 |
| Value Stream | 价值流分析 |
| Outcome Realization | 结果实现追溯 |

### 实施与迁移视角

| 视角 | 用途 |
|------|------|
| Project | 项目工作分解 |
| Migration | 迁移规划 |
| Implementation and Migration | 实施和迁移计划 |

## 建模最佳实践

### 1. 层次一致性

```
✓ 正确: 业务服务 → 应用服务 → 技术服务
✗ 错误: 业务流程直接调用技术节点
```

### 2. 关系方向

```
Serving 关系: 下层服务于上层
  技术服务 → 应用组件 → 业务流程

Realization 关系: 具体实现抽象
  应用组件 → 应用服务
```

### 3. 命名规范

| 元素类型 | 命名模式 | 示例 |
|----------|----------|------|
| Service | 动词 + 名词 | 订单处理服务 |
| Process | 动词 + 名词 | 处理订单 |
| Component | 名词 | 订单管理组件 |
| Object | 名词 | 订单 |

### 4. 粒度控制

- **战略视图**: 高层级抽象
- **概念视图**: 中等粒度
- **物理视图**: 详细实现

## 资源文件

- `references/elements-catalog.md` - 完整元素目录
- `references/relationships-matrix.md` - 关系矩阵
- `references/viewpoints-guide.md` - 视角使用指南

## 相关链接

- [ArchiMate 3.2 规范](https://pubs.opengroup.org/architecture/archimate32-doc/)
- [The Open Group ArchiMate Forum](https://www.opengroup.org/archimate-forum)
- [TOGAF 标准](https://www.opengroup.org/togaf)
- [DeepArchi 架构管理平台](https://www.deeparchi.com.cn)

## 关联技能

- `deeparchi` - ArchiMate 图表生成 (Draw.io)
- `togaf` - TOGAF 企业架构框架
