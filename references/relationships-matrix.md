# ArchiMate 3.2 关系矩阵

## 关系类型概览

### 1. 结构关系 (Structural Relationships)

#### Composition (组合)
```
符号: ◆────
方向: 从整体指向部分
含义: 强整体-部分关系，生命周期绑定
```

**有效组合示例:**
| 源元素 | 目标元素 |
|--------|----------|
| Application Component | Data Object |
| Node | Device |
| Business Role | Business Actor |

#### Aggregation (聚合)
```
符号: ◇────
方向: 从整体指向部分
含义: 弱整体-部分关系，生命周期独立
```

**有效聚合示例:**
| 源元素 | 目标元素 |
|--------|----------|
| Product | Business Service |
| Location | Business Actor |

#### Assignment (分配)
```
符号: ●────
方向: 从主动结构指向行为
含义: 将资源分配给行为执行
```

**有效分配示例:**
| 源元素 | 目标元素 |
|--------|----------|
| Business Role | Business Process |
| Application Component | Application Function |
| Node | Artifact |
| Device | System Software |

#### Realization (实现)
```
符号: ----▷
方向: 从具体指向抽象
含义: 具体元素实现抽象元素
```

**有效实现示例:**
| 源元素 | 目标元素 |
|--------|----------|
| Application Component | Application Service |
| Business Process | Business Service |
| Artifact | Data Object |
| Core Element | Requirement |

---

### 2. 依赖关系 (Dependency Relationships)

#### Serving (服务)
```
符号: ────▶
方向: 从提供者指向消费者
含义: 提供功能给另一元素使用
```

**跨层服务:**
```
Technology Service → Application Component
Application Service → Business Process
Business Service → Business Actor
```

#### Access (访问)
```
符号: ----▶ (虚线)
方向: 行为指向被动结构
含义: 行为读取或写入被动结构
修饰符: R(读), W(写), RW(读写)
```

**有效访问示例:**
| 源元素 | 目标元素 | 类型 |
|--------|----------|------|
| Business Process | Business Object | R/W |
| Application Function | Data Object | R/W |
| Application Service | Data Object | R/W |

#### Influence (影响)
```
符号: ----▶ (虚线)
方向: 影响源指向受影响者
含义: 影响动机元素
修饰符: + (正面), - (负面), 数字
```

**有效影响示例:**
| 源元素 | 目标元素 |
|--------|----------|
| Driver | Goal |
| Goal | Requirement |
| Constraint | Requirement |

#### Association (关联)
```
符号: ────
方向: 无方向（或双向）
含义: 通用关联关系
```

---

### 3. 动态关系 (Dynamic Relationships)

#### Triggering (触发)
```
符号: ────▶
方向: 从触发者指向被触发者
含义: 一个行为触发另一个行为
```

**有效触发示例:**
| 源元素 | 目标元素 |
|--------|----------|
| Business Event | Business Process |
| Business Process | Business Process |
| Application Event | Application Function |

#### Flow (流)
```
符号: ----▶ (虚线)
方向: 内容流动方向
含义: 在行为元素间传递内容
```

**有效流示例:**
| 源元素 | 目标元素 | 流动内容 |
|--------|----------|----------|
| Business Process | Business Process | Business Object |
| Application Function | Application Function | Data Object |

---

### 4. 其他关系 (Other Relationships)

#### Specialization (特化)
```
符号: ────▷
方向: 从特化指向通用
含义: 继承/特化关系
```

**示例:**
```
VIP Customer ----▷ Customer
Online Banking ----▷ Banking Service
```

#### Junction (连接点)
```
符号: ● (AND) 或 ○ (OR)
用途: 合并或分离关系
```

---

## 关系有效性矩阵

### 结构关系矩阵

| 关系 | 主动结构 | 行为 | 被动结构 |
|------|----------|------|----------|
| Composition | ✓ 同层/复合 | ✓ 同层 | ✓ 同层 |
| Aggregation | ✓ 同层/复合 | ✓ 同层 | ✓ 同层 |
| Assignment | ✓→行为 | - | - |
| Realization | ✓→服务 | ✓→服务 | ✓→对象 |

### 跨层关系规则

```
上层
  ↑ Serving (下层服务上层)
  ↑ Realization (下层实现上层)
下层

层次顺序 (从上到下):
1. Strategy
2. Business
3. Application
4. Technology
5. Physical
```

### 层间服务关系

| 源层 | 目标层 | 有效性 |
|------|--------|--------|
| Technology | Application | ✓ |
| Application | Business | ✓ |
| Business | Strategy | ✓ |
| Technology | Business | ✓ (跨层) |
| Application | Strategy | ✓ (跨层) |

---

## 关系使用最佳实践

### 1. 避免的反模式

```
✗ 业务流程直接分配给技术节点
✗ 数据对象之间使用触发关系
✗ 跳过中间层的服务关系（除非故意抽象）
```

### 2. 推荐模式

```
✓ 使用服务作为层间接口
✓ 行为元素通过服务暴露功能
✓ 主动结构通过分配关系执行行为
✓ 行为通过访问关系操作被动结构
```

### 3. 关系方向约定

| 关系类型 | 箭头方向 | 含义 |
|----------|----------|------|
| Serving | A → B | A 服务于 B |
| Realization | A → B | A 实现 B |
| Assignment | A → B | A 分配给 B |
| Triggering | A → B | A 触发 B |
| Access | A → B | A 访问 B |
| Flow | A → B | 内容从 A 流向 B |
