# ArchiMate 3.2 视角指南

## 视角概述

ArchiMate 视角 (Viewpoint) 定义了用于特定目的的元素和关系子集。每个视角针对特定利益相关者的关注点。

## 基础视角 (Basic Viewpoints)

### 1. Organization Viewpoint (组织视角)

**用途:** 展示组织结构及其与业务能力的关系

**包含元素:**
- Business Actor
- Business Role
- Business Collaboration
- Location
- Business Function

**典型用途:**
- 组织架构展示
- 职责分配分析
- 地理分布展示

**示例结构:**
```
┌─────────────────────────────────────┐
│           总公司 (Actor)             │
│  ┌─────────────┐ ┌─────────────┐    │
│  │   IT部门    │ │   业务部门   │   │
│  │   (Role)   │ │   (Role)    │    │
│  └─────────────┘ └─────────────┘    │
└─────────────────────────────────────┘
```

---

### 2. Business Process Cooperation Viewpoint (业务流程协作视角)

**用途:** 展示业务流程之间的协作关系

**包含元素:**
- Business Process
- Business Function
- Business Service
- Business Event
- Business Role
- Business Actor
- Business Object

**典型用途:**
- 端到端流程分析
- 流程改进
- 服务识别

---

### 3. Product Viewpoint (产品视角)

**用途:** 展示产品及其组成服务

**包含元素:**
- Product
- Business Service
- Application Service
- Contract
- Business Interface
- Value

**典型用途:**
- 产品组合管理
- 服务目录设计
- 价值分析

---

### 4. Application Cooperation Viewpoint (应用协作视角)

**用途:** 展示应用组件之间的协作关系

**包含元素:**
- Application Component
- Application Collaboration
- Application Interface
- Application Service
- Data Object
- Application Function

**典型用途:**
- 应用集成分析
- 接口设计
- 依赖分析

---

### 5. Application Usage Viewpoint (应用使用视角)

**用途:** 展示业务流程如何使用应用

**包含元素:**
- Business Process
- Business Role
- Application Service
- Application Interface
- Application Component
- Data Object

**典型用途:**
- 业务-IT对齐分析
- 应用覆盖分析
- 差距识别

---

### 6. Infrastructure Viewpoint (基础设施视角)

**用途:** 展示技术基础设施

**包含元素:**
- Node
- Device
- System Software
- Communication Network
- Path
- Technology Interface

**典型用途:**
- 基础设施规划
- 容量规划
- 灾备设计

---

### 7. Infrastructure Usage Viewpoint (基础设施使用视角)

**用途:** 展示应用如何使用基础设施

**包含元素:**
- Application Component
- Node
- System Software
- Technology Service
- Artifact

**典型用途:**
- 部署规划
- 资源优化
- 技术选型

---

### 8. Layered Viewpoint (分层视角)

**用途:** 展示多层架构的完整图景

**包含元素:**
- 所有层的元素
- 跨层关系

**典型用途:**
- 企业架构总览
- 影响分析
- 架构评审

**结构:**
```
┌─────────────────────────────────────┐
│            业务层                    │
│  Process ←── Service ←── Role       │
├─────────────────────────────────────┤
│            应用层                    │
│  Component ←── Service ←── Function │
├─────────────────────────────────────┤
│            技术层                    │
│  Node ←── System Software ←── Device│
└─────────────────────────────────────┘
```

---

## 动机视角 (Motivation Viewpoints)

### 9. Stakeholder Viewpoint (利益相关者视角)

**用途:** 展示利益相关者及其关注点

**包含元素:**
- Stakeholder
- Driver
- Assessment
- Goal
- Outcome

---

### 10. Goal Realization Viewpoint (目标实现视角)

**用途:** 展示目标如何通过需求和核心元素实现

**包含元素:**
- Goal
- Outcome
- Principle
- Requirement
- Constraint
- Core Elements (实现需求的元素)

---

### 11. Requirements Realization Viewpoint (需求实现视角)

**用途:** 展示需求如何被核心元素实现

**包含元素:**
- Requirement
- Constraint
- Goal
- Core Elements

---

### 12. Motivation Viewpoint (动机视角)

**用途:** 展示完整的动机结构

**包含元素:**
- 所有动机层元素
- 与核心元素的关系

---

## 策略视角 (Strategy Viewpoints)

### 13. Strategy Viewpoint (战略视角)

**用途:** 展示战略规划

**包含元素:**
- Resource
- Capability
- Course of Action
- Goal
- Outcome

---

### 14. Capability Map Viewpoint (能力地图视角)

**用途:** 展示组织能力的结构化视图

**包含元素:**
- Capability
- Resource
- Value Stream (可选)

**典型结构:**
```
┌───────────────────────────────────────────────────────┐
│                     企业能力                           │
├─────────────────┬─────────────────┬─────────────────┤
│   客户管理      │    运营管理      │    支撑能力      │
│  ┌───────────┐  │  ┌───────────┐  │  ┌───────────┐  │
│  │客户获取   │  │  │生产制造   │  │  │人力资源   │  │
│  │客户服务   │  │  │供应链管理 │  │  │财务管理   │  │
│  │客户分析   │  │  │质量管理   │  │  │IT管理     │  │
│  └───────────┘  │  └───────────┘  │  └───────────┘  │
└─────────────────┴─────────────────┴─────────────────┘
```

---

### 15. Value Stream Viewpoint (价值流视角)

**用途:** 展示端到端价值创造

**包含元素:**
- Value Stream
- Capability
- Resource
- Stakeholder
- Value

---

### 16. Outcome Realization Viewpoint (结果实现视角)

**用途:** 展示结果如何被实现

**包含元素:**
- Outcome
- Value
- Capability
- Course of Action

---

## 实施与迁移视角 (Implementation & Migration Viewpoints)

### 17. Project Viewpoint (项目视角)

**用途:** 展示项目及其交付物

**包含元素:**
- Work Package
- Deliverable
- Business Role
- Location

---

### 18. Migration Viewpoint (迁移视角)

**用途:** 展示架构演进

**包含元素:**
- Plateau
- Gap
- Core Elements (各阶段状态)

**典型结构:**
```
Baseline ──Gap──► Target State 1 ──Gap──► Target State 2
(Plateau)         (Plateau)              (Plateau)
```

---

### 19. Implementation and Migration Viewpoint (实施和迁移视角)

**用途:** 展示完整的实施计划

**包含元素:**
- Work Package
- Deliverable
- Plateau
- Gap
- Implementation Event

---

## 视角选择指南

### 按受众选择

| 受众 | 推荐视角 |
|------|----------|
| 高管/董事会 | Strategy, Capability Map, Value Stream |
| 业务负责人 | Product, Business Process Cooperation |
| IT架构师 | Layered, Application Cooperation, Infrastructure |
| 项目经理 | Project, Migration, Implementation |
| 合规/审计 | Requirements Realization, Goal Realization |

### 按目的选择

| 目的 | 推荐视角 |
|------|----------|
| 现状分析 | Layered, Organization, Infrastructure |
| 差距识别 | Migration, Gap Analysis |
| 影响评估 | Layered, Application Usage |
| 规划设计 | Strategy, Capability Map, Project |
| 服务设计 | Product, Service Realization |

---

## 自定义视角

ArchiMate 允许创建自定义视角，需要定义:

1. **目的**: 视角要回答什么问题
2. **利益相关者**: 谁是目标受众
3. **关注点**: 关注哪些方面
4. **元素集**: 包含哪些元素类型
5. **关系集**: 包含哪些关系类型

**示例 - 数据治理视角:**
```yaml
name: Data Governance Viewpoint
purpose: 展示数据资产及其治理结构
stakeholders:
  - Data Steward
  - Data Owner
  - Data Architect
elements:
  - Data Object
  - Application Component
  - Business Role
  - Business Process
  - Contract
relations:
  - Access
  - Assignment
  - Serving
```
