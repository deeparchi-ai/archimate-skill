# ArchiMate Skill - 企业架构建模语言

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![ArchiMate](https://img.shields.io/badge/ArchiMate-3.2-blue.svg)](https://www.opengroup.org/archimate)

## 概述

ArchiMate Skill 提供 ArchiMate 3.2 企业架构建模语言的完整参考。ArchiMate 是 The Open Group 维护的开放标准，用于企业架构的描述、分析和可视化。

## 功能特性

### 完整的元素覆盖

- **战略层 (Strategy)**: Resource, Capability, Value Stream, Course of Action
- **业务层 (Business)**: Actor, Role, Process, Service, Object, Event, Contract, Product
- **应用层 (Application)**: Component, Interface, Service, Function, Data Object
- **技术层 (Technology)**: Node, Device, System Software, Network, Artifact
- **物理层 (Physical)**: Facility, Equipment, Distribution Network, Material
- **实施迁移层 (I&M)**: Work Package, Deliverable, Plateau, Gap
- **动机层 (Motivation)**: Stakeholder, Driver, Goal, Requirement, Principle, Constraint

### 关系类型指南

- **结构关系**: Composition, Aggregation, Assignment, Realization
- **依赖关系**: Serving, Access, Influence, Association
- **动态关系**: Triggering, Flow
- **其他关系**: Specialization, Junction

### 视角定义

- 25+ 标准视角
- 基础视角、动机视角、策略视角、实施视角
- 自定义视角创建指南

## 使用场景

- 学习和理解 ArchiMate 建模语言
- 选择正确的元素类型进行建模
- 验证架构模型的合规性
- 设计架构视角和视图
- 与 TOGAF ADM 集成使用

## ArchiMate 3.2 核心框架

```
┌──────────────────────────────────────────────────────────────┐
│                        动机层                                 │
│        Stakeholder, Driver, Goal, Requirement                │
├───────────────┬──────────────────┬───────────────────────────┤
│   主动结构    │      行为        │        被动结构            │
├───────────────┼──────────────────┼───────────────────────────┤
│               │                  │                           │
│   战略层      │ Capability       │ Resource                  │
│               │ Value Stream     │ Course of Action          │
├───────────────┼──────────────────┼───────────────────────────┤
│               │                  │                           │
│   业务层      │ Process          │ Business Object           │
│   Actor/Role  │ Function/Service │ Contract/Product          │
├───────────────┼──────────────────┼───────────────────────────┤
│               │                  │                           │
│   应用层      │ App Function     │ Data Object               │
│   Component   │ App Service      │                           │
├───────────────┼──────────────────┼───────────────────────────┤
│               │                  │                           │
│   技术层      │ Tech Function    │ Artifact                  │
│   Node/Device │ Tech Service     │                           │
├───────────────┼──────────────────┼───────────────────────────┤
│               │                  │                           │
│   物理层      │                  │ Material                  │
│   Facility    │                  │ Equipment                 │
├───────────────┴──────────────────┴───────────────────────────┤
│                     实施与迁移层                               │
│          Work Package, Deliverable, Plateau, Gap             │
└──────────────────────────────────────────────────────────────┘
```

## 文件结构

```
archimate/
├── SKILL.md                        # 主技能文档
├── README.md                       # 本文件
├── package.json                    # 包配置
├── LICENSE                         # MIT 许可证
└── references/
    ├── elements-catalog.md         # 完整元素目录
    ├── relationships-matrix.md     # 关系有效性矩阵
    └── viewpoints-guide.md         # 视角使用指南
```

## 与其他技能的关系

| 技能 | 关系 | 说明 |
|------|------|------|
| deeparchi | 实现 | 使用 Draw.io 生成 ArchiMate 图 |
| togaf | 互补 | TOGAF ADM 的建模语言 |
| bian | 映射 | BIAN 服务域可映射到 ArchiMate |

## 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 相关资源

- [ArchiMate 3.2 Specification](https://pubs.opengroup.org/architecture/archimate32-doc/)
- [The Open Group ArchiMate Forum](https://www.opengroup.org/archimate-forum)
- [ArchiMate Exchange File Format](https://www.opengroup.org/open-group-archimate-model-exchange-file-format)
- [DeepArchi 架构管理平台](https://www.deeparchi.com.cn)

## 作者

DeepArchi Team
