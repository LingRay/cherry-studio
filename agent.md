# AI Agent 使用指南

## 概述

Cherry Studio 内置了多种 AI Agent，帮助用户完成各种任务。Agent 是预配置的 AI 助手，具有特定的技能和知识领域。每个 Agent 都经过精心设计，针对特定场景优化，能够提供更专业、更精准的帮助。

### 什么是 Agent？

Agent 是一个智能助手的预设配置，包含：

- **专业领域知识**：针对特定任务优化的系统提示词
- **模型配置**：适合该任务的 AI 模型和参数
- **工具集成**：可能包含代码执行、网络搜索等工具
- **交互方式**：优化的温度参数和响应长度

### Agent vs 普通对话

| 特性     | Agent            | 普通对话     |
| -------- | ---------------- | ------------ |
| 专业性   | 针对特定领域优化 | 通用型回答   |
| 一致性   | 保持角色设定     | 可能变化     |
| 工具支持 | 预配置工具集     | 需手动指定   |
| 效率     | 更快达成目标     | 需要更多指导 |

## Agent 类型

### 1. 编程助手 (Programming Assistant)

- **功能**: 代码编写、调试、重构、代码审查
- **适用场景**:
  - 软件开发和架构设计
  - 代码问题诊断和修复
  - 算法优化和性能调优
  - 单元测试编写
- **特点**:
  - 熟悉多种编程语言（JavaScript/TypeScript, Python, Java, Go, Rust 等）
  - 了解主流框架（React, Vue, Express, Django 等）
  - 遵循代码最佳实践和设计模式
- **推荐模型**: GPT-4, Claude-3-Opus
- **温度设置**: 0.3-0.5（更注重准确性）

### 2. 文档撰写 (Documentation Writer)

- **功能**: 技术文档、API 文档、用户手册编写
- **适用场景**:
  - 项目 README 文档
  - API 接口文档
  - 用户操作指南
  - 技术规范说明
- **特点**:
  - 结构化思维，层次清晰
  - 语言简洁准确
  - 支持 Markdown、reStructuredText 等格式
- **推荐模型**: GPT-4, Claude-3-Sonnet
- **温度设置**: 0.5-0.7

### 3. 数据分析师 (Data Analyst)

- **功能**: 数据处理、可视化、统计分析、报告生成
- **适用场景**:
  - 业务数据分析
  - 数据清洗和预处理
  - 可视化图表制作
  - 趋势预测和模式识别
- **特点**:
  - 熟悉 Python 数据分析库（Pandas, NumPy, Matplotlib）
  - 统计学知识丰富
  - 能够解释复杂数据模式
- **推荐模型**: GPT-4, Claude-3-Opus
- **温度设置**: 0.4-0.6
- **工具**: Code Interpreter

### 4. 产品经理 (Product Manager)

- **功能**: 需求分析、产品规划、用户研究、竞品分析
- **适用场景**:
  - 产品需求文档（PRD）编写
  - 用户故事和用例设计
  - 功能优先级排序
  - 产品路线图规划
- **特点**:
  - 用户导向，注重用户体验
  - 商业思维，平衡需求和资源
  - 数据驱动决策
- **推荐模型**: GPT-4, Claude-3-Sonnet
- **温度设置**: 0.6-0.8

### 5. 翻译专家 (Translation Expert)

- **功能**: 多语言翻译、本地化、术语管理
- **适用场景**:
  - 技术文档翻译
  - 用户界面本地化
  - 多语言内容管理
  - 术语表维护
- **特点**:
  - 支持多种语言对
  - 保持专业术语一致性
  - 考虑文化差异
  - 语言地道自然
- **推荐模型**: GPT-4, Claude-3-Sonnet
- **温度设置**: 0.3-0.5

### 6. UI/UX 设计师 (UI/UX Designer)

- **功能**: 界面设计、用户体验优化、设计系统
- **适用场景**:
  - 界面布局设计
  - 交互流程优化
  - 设计规范制定
  - 可访问性改进
- **特点**:
  - 熟悉设计原则和模式
  - 了解前端技术实现
  - 关注用户体验
- **推荐模型**: GPT-4, Claude-3-Opus
- **温度设置**: 0.7-0.9

### 7. DevOps 工程师 (DevOps Engineer)

- **功能**: CI/CD、容器化、监控、自动化部署
- **适用场景**:
  - 构建流水线设计
  - Docker/Kubernetes 配置
  - 监控告警设置
  - 基础设施即代码
- **特点**:
  - 熟悉云平台（AWS, Azure, GCP）
  - 掌握自动化工具
  - 重视系统可靠性
- **推荐模型**: GPT-4, Claude-3-Opus
- **温度设置**: 0.3-0.5

### 8. 安全专家 (Security Expert)

- **功能**: 安全审计、漏洞分析、安全加固
- **适用场景**:
  - 代码安全审查
  - 漏洞修复建议
  - 安全最佳实践
  - 渗透测试辅助
- **特点**:
  - 了解常见安全漏洞（OWASP Top 10）
  - 熟悉加密和认证机制
  - 重视数据隐私
- **推荐模型**: GPT-4, Claude-3-Opus
- **温度设置**: 0.2-0.4

### 9. 教育导师 (Educational Tutor)

- **功能**: 知识讲解、概念解释、学习指导
- **适用场景**:
  - 编程基础教学
  - 技术概念解释
  - 学习路径规划
  - 练习题生成
- **特点**:
  - 耐心细致
  - 循序渐进
  - 提供实例和类比
- **推荐模型**: GPT-4, Claude-3-Sonnet
- **温度设置**: 0.6-0.8

### 10. 内容创作者 (Content Creator)

- **功能**: 博客写作、社交媒体内容、营销文案
- **适用场景**:
  - 技术博客文章
  - 社交媒体帖子
  - 产品介绍文案
  - SEO 优化内容
- **特点**:
  - 创意丰富
  - 吸引读者注意
  - 符合 SEO 规范
- **推荐模型**: GPT-4, Claude-3-Sonnet
- **温度设置**: 0.7-0.9

## 使用方法

### 快速开始

#### 选择 Agent

1. 在聊天界面点击顶部的 **Agent 选择器**
2. 浏览可用的 Agent 列表
3. 点击选择适合当前任务的 Agent
4. 开始对话

#### 切换 Agent

- 在对话过程中，可以随时切换到其他 Agent
- 切换 Agent 会保留对话历史，但会应用新的系统提示词
- 建议在切换时告知 Agent 之前的上下文

### 高级用法

#### 组合使用多个 Agent

针对复杂任务，可以组合使用多个 Agent：

1. **需求分析** → 产品经理 Agent
2. **技术设计** → 编程助手 Agent
3. **文档编写** → 文档撰写 Agent
4. **多语言支持** → 翻译专家 Agent

#### 与工具配合

某些 Agent 可以使用工具增强能力：

- **代码解释器**: 数据分析师、编程助手
- **网络搜索**: 内容创作者、产品经理
- **文件操作**: 文档撰写、编程助手

#### 提示词技巧

与 Agent 对话时的最佳实践：

```markdown
# 好的提示词示例

我需要优化这段 Python 代码的性能。代码功能是处理大量 CSV 文件数据。
当前问题：处理 1GB 数据需要 30 分钟。
期望：希望能在 5 分钟内完成。

# 不好的提示词示例

帮我优化代码。
```

**提示词要素**：

- ✅ 明确的目标
- ✅ 具体的上下文
- ✅ 可衡量的指标
- ✅ 限制和约束条件
- ❌ 模糊的需求
- ❌ 缺少背景信息

### 自定义 Agent

#### 创建自定义 Agent

```json
{
  "id": "custom-assistant",
  "name": "自定义助手",
  "description": "专门处理特定任务的助手",
  "avatar": "🤖",
  "model": "gpt-4",
  "systemPrompt": "你是一个专业的区块链开发专家，精通 Solidity、Web3.js 和智能合约开发。你的职责是帮助用户设计、开发和审计智能合约。",
  "temperature": 0.5,
  "maxTokens": 4096,
  "tools": ["code_interpreter"],
  "tags": ["区块链", "智能合约", "Solidity"]
}
```

#### 系统提示词模板

```text
# 角色定义
你是一个 {专业领域} 的专家，拥有 {年限} 年的经验。

# 核心能力
- 能力 1: {具体描述}
- 能力 2: {具体描述}
- 能力 3: {具体描述}

# 工作方式
1. 仔细分析用户需求
2. 提供结构化的解决方案
3. 给出具体可执行的步骤
4. 解释关键决策的理由

# 输出格式
- 使用 Markdown 格式
- 代码使用适当的语法高亮
- 重要信息使用加粗或列表

# 限制条件
- 不提供 {禁止内容}
- 遵守 {行业规范}
- 保持专业和准确
```

#### 导入/导出 Agent

```typescript
// 导出 Agent 配置
function exportAgent(agent: Agent): string {
  return JSON.stringify(agent, null, 2);
}

// 导入 Agent 配置
function importAgent(configJson: string): Agent {
  return JSON.parse(configJson);
}

// 批量导入
function importAgents(configFile: string): Agent[] {
  const data = fs.readFileSync(configFile, "utf-8");
  return JSON.parse(data).agents;
}
```

## 配置文件

Agent 配置存储在以下位置：

- **中文版本**: `resources/data/agents-zh.json`
- **英文版本**: `resources/data/agents-en.json`
- **用户自定义**: `~/.cherry-studio/agents.json`

### 配置文件结构

```json
{
  "version": "2.0",
  "agents": [
    {
      "id": "programming-assistant",
      "name": "编程助手",
      "nameEn": "Programming Assistant",
      "description": "专业的编程和开发助手，精通多种编程语言和框架",
      "descriptionEn": "Professional programming and development assistant",
      "avatar": "🧑‍💻",
      "model": "gpt-4-turbo-preview",
      "systemPrompt": "你是一个经验丰富的软件工程师...",
      "temperature": 0.3,
      "maxTokens": 4096,
      "topP": 1.0,
      "frequencyPenalty": 0.0,
      "presencePenalty": 0.0,
      "tools": ["code_interpreter", "web_search"],
      "tags": ["编程", "开发", "调试"],
      "category": "development",
      "enabled": true,
      "builtin": true,
      "createdAt": "2024-01-01T00:00:00.000Z",
      "updatedAt": "2024-01-01T00:00:00.000Z"
    }
  ]
}
```

### 配置字段说明

| 字段               | 类型     | 必填 | 说明                     |
| ------------------ | -------- | ---- | ------------------------ |
| `id`               | string   | ✅   | Agent 唯一标识符         |
| `name`             | string   | ✅   | Agent 名称（中文）       |
| `nameEn`           | string   | ❌   | Agent 名称（英文）       |
| `description`      | string   | ✅   | Agent 描述               |
| `avatar`           | string   | ❌   | Emoji 头像               |
| `model`            | string   | ✅   | 使用的 AI 模型           |
| `systemPrompt`     | string   | ✅   | 系统提示词               |
| `temperature`      | number   | ❌   | 温度参数 (0-2)，默认 0.7 |
| `maxTokens`        | number   | ❌   | 最大令牌数，默认 2048    |
| `topP`             | number   | ❌   | Top-P 采样，默认 1.0     |
| `frequencyPenalty` | number   | ❌   | 频率惩罚，默认 0.0       |
| `presencePenalty`  | number   | ❌   | 存在惩罚，默认 0.0       |
| `tools`            | string[] | ❌   | 可用工具列表             |
| `tags`             | string[] | ❌   | 标签分类                 |
| `category`         | string   | ❌   | 所属类别                 |
| `enabled`          | boolean  | ❌   | 是否启用，默认 true      |
| `builtin`          | boolean  | ❌   | 是否为内置 Agent         |

### 温度参数指南

温度参数影响输出的随机性和创造性：

| 温度范围 | 特点                   | 适用场景                 |
| -------- | ---------------------- | ------------------------ |
| 0.0-0.3  | 确定性强，输出一致     | 代码生成、数据分析、翻译 |
| 0.3-0.5  | 平衡准确性和灵活性     | 技术文档、问题解答       |
| 0.5-0.7  | 适度创造性             | 产品设计、教学辅导       |
| 0.7-0.9  | 创造性强，多样性高     | 内容创作、头脑风暴       |
| 0.9-1.5  | 高度创造性，可能不连贯 | 艺术创作、实验性探索     |

### 模型选择指南

| 模型            | 优势               | 劣势             | 推荐场景           |
| --------------- | ------------------ | ---------------- | ------------------ |
| GPT-4 Turbo     | 能力最强，上下文长 | 成本高，速度较慢 | 复杂任务、长文档   |
| GPT-4           | 准确度高           | 成本高           | 专业任务           |
| GPT-3.5 Turbo   | 速度快，成本低     | 能力有限         | 简单任务、快速交互 |
| Claude-3-Opus   | 擅长分析和推理     | 成本较高         | 代码审查、深度分析 |
| Claude-3-Sonnet | 平衡性能和成本     | -                | 通用任务           |
| Claude-3-Haiku  | 速度极快           | 能力一般         | 简单查询           |

## 最佳实践

### 1. 明确任务目标

在开始对话前，清晰定义你的目标：

**✅ 好的示例**：

```
我需要为一个 TypeScript React 项目创建一个可复用的表单验证 Hook。
要求：
- 支持多种验证规则（必填、邮箱、长度等）
- 实时验证和提交时验证
- 显示错误信息
- TypeScript 类型安全
```

**❌ 不好的示例**：

```
帮我写个表单验证
```

### 2. 逐步细化需求

采用迭代方式逐步完善：

**第一步 - 整体框架**：

```
设计一个用户认证系统的整体架构
```

**第二步 - 具体实现**：

```
实现 JWT 令牌的生成和验证逻辑
```

**第三步 - 优化改进**：

```
添加令牌刷新机制和过期处理
```

### 3. 利用 Agent 专长

根据任务特点选择合适的 Agent：

| 任务类型     | 推荐 Agent    | 理由           |
| ------------ | ------------- | -------------- |
| 修复 Bug     | 编程助手      | 代码诊断能力强 |
| 写 API 文档  | 文档撰写      | 结构化表达能力 |
| 分析用户数据 | 数据分析师    | 统计分析专长   |
| 设计新功能   | 产品经理      | 用户需求理解   |
| 优化部署流程 | DevOps 工程师 | 运维经验丰富   |

### 4. 提供足够上下文

让 Agent 了解完整的背景信息：

```markdown
## 项目背景

- 技术栈：Next.js 14 + TypeScript + Tailwind CSS
- 目标用户：企业级客户
- 当前问题：首页加载时间超过 3 秒

## 已尝试的方案

1. 启用了图片懒加载
2. 使用了动态导入

## 期望结果

- 首屏加载时间 < 1.5 秒
- 保持现有功能不变
```

### 5. 迭代优化

根据输出结果持续改进：

**迭代流程**：

1. 获取初始方案
2. 测试验证
3. 反馈问题
4. 调整优化
5. 重复 2-4 直到满意

**反馈示例**：

```
这个方案整体不错，但有两个问题：
1. 性能上：在处理大数组时会卡顿
2. 可读性：变量命名不够清晰

能否针对这两点优化一下？
```

### 6. 使用代码块和格式

清晰地组织信息：

````markdown
### 问题代码

```typescript
// 存在性能问题的代码
const result = data.map((item) => {
  return heavyComputation(item);
});
```

### 期望改进

- 使用 Web Worker 处理计算
- 添加进度指示
- 支持取消操作
````

### 7. 分阶段处理复杂任务

将大任务拆分为小步骤：

**任务**：开发一个完整的博客系统

**拆分方案**：

1. 数据模型设计（数据分析师）
2. API 接口设计（编程助手）
3. 前端组件开发（编程助手 + UI/UX 设计师）
4. 用户认证实现（安全专家）
5. 部署配置（DevOps 工程师）
6. 文档编写（文档撰写）

### 8. 版本控制和实验

保存不同的解决方案版本：

```typescript
// 方案 A：性能优先
function optimizedVersion() {
  // 使用缓存和记忆化
}

// 方案 B：可读性优先
function readableVersion() {
  // 清晰的逻辑流程
}

// 方案 C：平衡方案
function balancedVersion() {
  // 综合考虑
}
```

### 9. 学习和记录

记录有价值的对话和解决方案：

- 📝 创建个人知识库
- 🏷️ 为对话添加标签
- ⭐ 收藏优秀的回答
- 🔄 定期回顾和总结

### 10. 安全和隐私

保护敏感信息：

**❌ 避免**：

```typescript
const API_KEY = "sk-proj-abc123xyz..."; // 真实密钥
const PASSWORD = "mypassword123"; // 真实密码
```

**✅ 推荐**：

```typescript
const API_KEY = "sk-proj-xxx..."; // 使用占位符
const PASSWORD = "********"; // 隐藏敏感信息
```

## 开发指南

### Agent 架构

```typescript
// Agent 接口定义
interface Agent {
  id: string; // 唯一标识
  name: string; // 显示名称
  description: string; // 描述信息
  avatar?: string; // 头像（Emoji）
  model: string; // AI 模型
  systemPrompt: string; // 系统提示词
  temperature?: number; // 温度参数
  maxTokens?: number; // 最大令牌数
  topP?: number; // Top-P 采样
  frequencyPenalty?: number; // 频率惩罚
  presencePenalty?: number; // 存在惩罚
  tools?: AgentTool[]; // 工具集合
  tags?: string[]; // 标签
  category?: string; // 分类
  enabled?: boolean; // 是否启用
  builtin?: boolean; // 是否内置
  metadata?: AgentMetadata; // 元数据
}

// 工具定义
interface AgentTool {
  type: "code_interpreter" | "web_search" | "file_operation" | "custom";
  enabled: boolean;
  config?: Record<string, any>;
}

// 元数据
interface AgentMetadata {
  author?: string;
  version?: string;
  createdAt?: string;
  updatedAt?: string;
  usage?: number;
  rating?: number;
}
```

### 创建新 Agent

#### 1. 定义 Agent 配置

```typescript
const newAgent: Agent = {
  id: "blockchain-expert",
  name: "区块链专家",
  description: "精通区块链技术和智能合约开发",
  avatar: "⛓️",
  model: "gpt-4-turbo-preview",
  systemPrompt: `你是一个资深的区块链技术专家，拥有以下专长：

## 专业领域
- 智能合约开发（Solidity, Vyper）
- 区块链架构设计
- DeFi 协议开发
- NFT 和代币标准（ERC-20, ERC-721, ERC-1155）
- 安全审计和最佳实践

## 工作方式
1. 分析需求，识别关键技术挑战
2. 提供安全、高效的解决方案
3. 解释技术决策和权衡
4. 强调安全性和 Gas 优化

## 输出规范
- 代码使用 Solidity 0.8.x 版本
- 遵循 OpenZeppelin 标准
- 包含详细的注释
- 提供测试建议

## 安全优先
- 检查重入攻击
- 验证输入参数
- 使用安全的数学运算
- 遵循检查-效果-交互模式`,
  temperature: 0.3,
  maxTokens: 4096,
  tools: [
    {
      type: "code_interpreter",
      enabled: true,
    },
  ],
  tags: ["区块链", "Solidity", "智能合约", "Web3"],
  category: "development",
  enabled: true,
  builtin: false,
  metadata: {
    author: "Cherry Studio Team",
    version: "1.0.0",
    createdAt: new Date().toISOString(),
  },
};
```

#### 2. 系统提示词最佳实践

**结构化模板**：

```markdown
# 角色定义

你是 {具体角色}，拥有 {专业背景}。

# 核心能力

## 技术能力

- 能力 1
- 能力 2
- 能力 3

## 软技能

- 沟通能力
- 问题解决
- 教学能力

# 工作流程

1. 理解需求
2. 分析问题
3. 提出方案
4. 实施验证
5. 优化改进

# 输出标准

- 格式：Markdown
- 代码：带语法高亮
- 结构：清晰分层
- 解释：通俗易懂

# 限制条件

- 不做：{禁止项}
- 必须：{必须项}
- 遵守：{规范}

# 特殊要求

- {场景特定要求}
```

**示例：数据科学家 Agent**：

```text
# 角色定义
你是一位经验丰富的数据科学家，专注于数据分析、机器学习和统计建模。

# 核心能力
## 技术栈
- Python 数据分析库（Pandas, NumPy, SciPy）
- 机器学习框架（Scikit-learn, TensorFlow, PyTorch）
- 数据可视化（Matplotlib, Seaborn, Plotly）
- SQL 和数据库操作
- 统计分析和假设检验

## 分析方法
- 探索性数据分析（EDA）
- 特征工程
- 模型选择和调优
- A/B 测试
- 时间序列分析

# 工作流程
1. **数据理解**：询问数据来源、特征、目标
2. **数据探索**：统计描述、分布分析、相关性
3. **问题定义**：明确分析目标和成功指标
4. **方法选择**：选择合适的算法和技术
5. **结果解释**：用业务语言解释技术结果

# 输出标准
- 使用 Python 代码示例
- 提供可视化建议
- 解释统计显著性
- 给出可执行建议
- 注明假设和局限性

# 代码规范
- 使用 type hints
- 添加文档字符串
- 处理缺失值和异常
- 优化计算效率
- 可重现的随机种子

# 沟通方式
- 避免过度技术术语
- 使用类比和实例
- 可视化辅助说明
- 提供多个方案对比
```

#### 3. Agent 管理类

```typescript
class AgentManager {
  private agents: Map<string, Agent> = new Map();
  private configPath: string;

  constructor(configPath: string) {
    this.configPath = configPath;
    this.loadAgents();
  }

  // 加载 Agent 配置
  loadAgents(): void {
    try {
      const config = JSON.parse(fs.readFileSync(this.configPath, "utf-8"));
      config.agents.forEach((agent: Agent) => {
        this.agents.set(agent.id, agent);
      });
      console.log(`已加载 ${this.agents.size} 个 Agent`);
    } catch (error) {
      console.error("加载 Agent 配置失败:", error);
    }
  }

  // 保存 Agent 配置
  saveAgents(): void {
    try {
      const config = {
        version: "2.0",
        agents: Array.from(this.agents.values()),
      };
      fs.writeFileSync(
        this.configPath,
        JSON.stringify(config, null, 2),
        "utf-8"
      );
      console.log("Agent 配置已保存");
    } catch (error) {
      console.error("保存 Agent 配置失败:", error);
    }
  }

  // 获取 Agent
  getAgent(id: string): Agent | undefined {
    return this.agents.get(id);
  }

  // 获取所有 Agent
  getAllAgents(): Agent[] {
    return Array.from(this.agents.values());
  }

  // 按分类获取
  getAgentsByCategory(category: string): Agent[] {
    return this.getAllAgents().filter((agent) => agent.category === category);
  }

  // 按标签搜索
  searchAgentsByTag(tag: string): Agent[] {
    return this.getAllAgents().filter((agent) => agent.tags?.includes(tag));
  }

  // 添加 Agent
  addAgent(agent: Agent): void {
    if (this.agents.has(agent.id)) {
      throw new Error(`Agent ${agent.id} 已存在`);
    }
    this.agents.set(agent.id, {
      ...agent,
      metadata: {
        ...agent.metadata,
        createdAt: new Date().toISOString(),
      },
    });
    this.saveAgents();
  }

  // 更新 Agent
  updateAgent(id: string, updates: Partial<Agent>): void {
    const agent = this.agents.get(id);
    if (!agent) {
      throw new Error(`Agent ${id} 不存在`);
    }
    this.agents.set(id, {
      ...agent,
      ...updates,
      metadata: {
        ...agent.metadata,
        ...updates.metadata,
        updatedAt: new Date().toISOString(),
      },
    });
    this.saveAgents();
  }

  // 删除 Agent
  deleteAgent(id: string): void {
    const agent = this.agents.get(id);
    if (agent?.builtin) {
      throw new Error("不能删除内置 Agent");
    }
    this.agents.delete(id);
    this.saveAgents();
  }

  // 验证 Agent 配置
  validateAgent(agent: Agent): boolean {
    const required = ["id", "name", "description", "model", "systemPrompt"];
    for (const field of required) {
      if (!agent[field as keyof Agent]) {
        throw new Error(`缺少必填字段: ${field}`);
      }
    }

    if (agent.temperature !== undefined) {
      if (agent.temperature < 0 || agent.temperature > 2) {
        throw new Error("temperature 必须在 0-2 之间");
      }
    }

    if (agent.maxTokens !== undefined && agent.maxTokens < 1) {
      throw new Error("maxTokens 必须大于 0");
    }

    return true;
  }

  // 克隆 Agent
  cloneAgent(id: string, newId: string, newName: string): Agent {
    const original = this.agents.get(id);
    if (!original) {
      throw new Error(`Agent ${id} 不存在`);
    }

    const cloned: Agent = {
      ...JSON.parse(JSON.stringify(original)),
      id: newId,
      name: newName,
      builtin: false,
      metadata: {
        author: original.metadata?.author,
        version: "1.0.0",
        createdAt: new Date().toISOString(),
      },
    };

    this.addAgent(cloned);
    return cloned;
  }

  // 导出 Agent
  exportAgent(id: string, filePath: string): void {
    const agent = this.agents.get(id);
    if (!agent) {
      throw new Error(`Agent ${id} 不存在`);
    }
    fs.writeFileSync(filePath, JSON.stringify(agent, null, 2), "utf-8");
  }

  // 导入 Agent
  importAgent(filePath: string): void {
    const agentData = JSON.parse(fs.readFileSync(filePath, "utf-8"));
    this.validateAgent(agentData);
    this.addAgent(agentData);
  }
}
```

#### 4. Agent 实例化

```typescript
class AgentInstance {
  private agent: Agent;
  private conversationHistory: Message[] = [];
  private model: AIModel;

  constructor(agent: Agent, model: AIModel) {
    this.agent = agent;
    this.model = model;
  }

  // 处理用户输入
  async process(userInput: string): Promise<string> {
    // 添加系统提示词
    const messages: Message[] = [
      {
        role: "system",
        content: this.agent.systemPrompt,
      },
      ...this.conversationHistory,
      {
        role: "user",
        content: userInput,
      },
    ];

    // 调用 AI 模型
    const response = await this.model.chat({
      messages,
      temperature: this.agent.temperature ?? 0.7,
      maxTokens: this.agent.maxTokens ?? 2048,
      topP: this.agent.topP,
      frequencyPenalty: this.agent.frequencyPenalty,
      presencePenalty: this.agent.presencePenalty,
    });

    // 更新对话历史
    this.conversationHistory.push(
      { role: "user", content: userInput },
      { role: "assistant", content: response }
    );

    return response;
  }

  // 重置对话
  reset(): void {
    this.conversationHistory = [];
  }

  // 获取对话历史
  getHistory(): Message[] {
    return [...this.conversationHistory];
  }

  // 使用工具
  async useTool(toolType: string, params: any): Promise<any> {
    const tool = this.agent.tools?.find((t) => t.type === toolType);
    if (!tool || !tool.enabled) {
      throw new Error(`工具 ${toolType} 不可用`);
    }

    // 工具调用逻辑
    switch (toolType) {
      case "code_interpreter":
        return await this.executeCode(params);
      case "web_search":
        return await this.searchWeb(params);
      default:
        throw new Error(`未知工具类型: ${toolType}`);
    }
  }

  private async executeCode(params: any): Promise<any> {
    // 代码执行逻辑
  }

  private async searchWeb(params: any): Promise<any> {
    // 网络搜索逻辑
  }
}
```

### 测试 Agent

```typescript
describe("Agent Tests", () => {
  let manager: AgentManager;

  beforeEach(() => {
    manager = new AgentManager("./test-agents.json");
  });

  test("应该能够加载 Agent", () => {
    const agents = manager.getAllAgents();
    expect(agents.length).toBeGreaterThan(0);
  });

  test("应该能够创建新 Agent", () => {
    const newAgent: Agent = {
      id: "test-agent",
      name: "测试助手",
      description: "用于测试的 Agent",
      model: "gpt-4",
      systemPrompt: "你是一个测试助手",
    };

    manager.addAgent(newAgent);
    const retrieved = manager.getAgent("test-agent");
    expect(retrieved).toBeDefined();
    expect(retrieved?.name).toBe("测试助手");
  });

  test("应该验证 Agent 配置", () => {
    const invalidAgent: any = {
      id: "invalid",
      name: "无效 Agent",
      // 缺少必填字段
    };

    expect(() => manager.validateAgent(invalidAgent)).toThrow();
  });

  test("应该能够更新 Agent", () => {
    manager.updateAgent("test-agent", {
      description: "更新后的描述",
    });

    const updated = manager.getAgent("test-agent");
    expect(updated?.description).toBe("更新后的描述");
  });

  test("不应该删除内置 Agent", () => {
    expect(() => manager.deleteAgent("programming-assistant")).toThrow();
  });
});
```

## 故障排除

### 常见问题

#### 1. Agent 响应不准确

**症状**：

- Agent 的回答偏离主题
- 输出质量不稳定
- 理解错误用户意图

**可能原因**：

- 系统提示词不够明确
- Temperature 参数设置不当
- 缺少必要上下文

**解决方案**：

```typescript
// ❌ 不好的提示词
systemPrompt: "你是一个助手";

// ✅ 改进的提示词
systemPrompt: `你是一个专业的前端开发助手，专注于 React 和 TypeScript。

## 核心职责
1. 提供准确的代码示例
2. 解释技术概念
3. 遵循最佳实践

## 回答规范
- 使用 TypeScript 严格模式
- 遵循 React Hooks 规范
- 提供可运行的代码
- 解释关键决策

## 限制
- 不使用过时的 API
- 不推荐不安全的做法`;
```

**调整参数**：

```typescript
// 对于需要精确输出的任务
temperature: 0.2 - 0.4;

// 对于需要创造性的任务
temperature: 0.7 - 0.9;
```

#### 2. Agent 无法访问工具

**症状**：

- 工具调用失败
- 提示"工具不可用"
- 功能受限

**检查清单**：

```typescript
// 1. 确认工具已启用
const agent: Agent = {
  // ...
  tools: [
    {
      type: "code_interpreter",
      enabled: true, // ✅ 确保为 true
      config: {
        // 工具特定配置
      },
    },
  ],
};

// 2. 检查工具配置
const toolConfig = {
  timeout: 30000, // 超时时间
  maxMemory: 512, // 最大内存（MB）
  allowedPackages: [], // 允许的包
};

// 3. 验证权限
if (!hasToolPermission(user, "code_interpreter")) {
  throw new Error("没有工具使用权限");
}
```

**解决步骤**：

1. 检查 Agent 配置中的 `tools` 字段
2. 验证工具服务是否运行
3. 查看错误日志获取详细信息
4. 确认 API 密钥和权限设置

#### 3. 性能问题

**症状**：

- 响应时间过长
- 消耗过多 Token
- 频繁超时

**优化策略**：

**a) 优化 maxTokens 设置**

```typescript
// ❌ 过大的设置
maxTokens: 8192; // 可能导致响应慢、成本高

// ✅ 根据实际需求设置
const taskTokenLimits = {
  "simple-query": 500,
  "code-generation": 2048,
  "document-writing": 4096,
  "complex-analysis": 8192,
};
```

**b) 选择合适的模型**

```typescript
interface ModelSelection {
  task: string;
  complexity: "low" | "medium" | "high";
  recommendedModel: string;
}

const modelGuide: ModelSelection[] = [
  {
    task: "简单问答",
    complexity: "low",
    recommendedModel: "gpt-3.5-turbo",
  },
  {
    task: "代码生成",
    complexity: "medium",
    recommendedModel: "gpt-4",
  },
  {
    task: "复杂分析",
    complexity: "high",
    recommendedModel: "gpt-4-turbo",
  },
];
```

**c) 实现缓存机制**

```typescript
class AgentCache {
  private cache = new Map<string, CacheEntry>();
  private ttl = 3600000; // 1小时

  async get(key: string): Promise<string | null> {
    const entry = this.cache.get(key);
    if (!entry) return null;

    if (Date.now() - entry.timestamp > this.ttl) {
      this.cache.delete(key);
      return null;
    }

    return entry.value;
  }

  set(key: string, value: string): void {
    this.cache.set(key, {
      value,
      timestamp: Date.now(),
    });
  }

  // 生成缓存键
  generateKey(agent: Agent, input: string): string {
    return `${agent.id}:${hashString(input)}`;
  }
}
```

**d) 减少不必要的工具调用**

```typescript
class SmartAgent extends AgentInstance {
  async process(input: string): Promise<string> {
    // 分析是否需要工具
    const needsTool = this.analyzeToolRequirement(input);

    if (!needsTool) {
      // 直接使用对话模型
      return await this.chatOnly(input);
    }

    // 只在必要时使用工具
    return await this.processWithTools(input);
  }

  private analyzeToolRequirement(input: string): boolean {
    const toolKeywords = [
      "execute",
      "run",
      "calculate",
      "search",
      "执行",
      "运行",
      "计算",
      "搜索",
    ];
    return toolKeywords.some((kw) => input.toLowerCase().includes(kw));
  }
}
```

#### 4. 对话上下文丢失

**症状**：

- Agent 忘记之前的对话
- 无法引用历史信息
- 重复询问相同问题

**解决方案**：

```typescript
class ContextManager {
  private maxHistoryLength = 20;
  private maxTokens = 4000;

  // 智能裁剪历史
  trimHistory(history: Message[]): Message[] {
    // 保留系统消息
    const systemMsg = history.find((m) => m.role === "system");
    let messages = history.filter((m) => m.role !== "system");

    // 按 Token 数量裁剪
    let totalTokens = this.estimateTokens(messages);
    while (totalTokens > this.maxTokens && messages.length > 2) {
      messages.shift(); // 移除最早的消息
      totalTokens = this.estimateTokens(messages);
    }

    // 确保保留最近的对话
    if (messages.length > this.maxHistoryLength) {
      messages = messages.slice(-this.maxHistoryLength);
    }

    return systemMsg ? [systemMsg, ...messages] : messages;
  }

  // 估算 Token 数量
  private estimateTokens(messages: Message[]): number {
    return messages.reduce((sum, msg) => {
      return sum + Math.ceil(msg.content.length / 4);
    }, 0);
  }

  // 摘要压缩
  async summarizeHistory(history: Message[]): Promise<Message> {
    const summary = await this.generateSummary(history);
    return {
      role: "system",
      content: `之前对话摘要：${summary}`,
    };
  }
}
```

#### 5. 编码和特殊字符问题

**症状**：

- 显示乱码
- 特殊字符丢失
- JSON 解析失败

**解决方案**：

```typescript
class TextProcessor {
  // 清理文本
  sanitize(text: string): string {
    return text
      .replace(/[\u0000-\u001F\u007F-\u009F]/g, "") // 移除控制字符
      .replace(/\r\n/g, "\n") // 统一换行符
      .trim();
  }

  // 转义特殊字符
  escapeForJSON(text: string): string {
    return text
      .replace(/\\/g, "\\\\")
      .replace(/"/g, '\\"')
      .replace(/\n/g, "\\n")
      .replace(/\r/g, "\\r")
      .replace(/\t/g, "\\t");
  }

  // 安全解析 JSON
  safeJSONParse(text: string): any {
    try {
      return JSON.parse(text);
    } catch (error) {
      console.error("JSON 解析失败:", error);
      // 尝试修复常见问题
      const fixed = text
        .replace(/,(\s*[}\]])/g, "$1") // 移除尾部逗号
        .replace(/'/g, '"'); // 替换单引号
      return JSON.parse(fixed);
    }
  }
}
```

#### 6. API 限流和配额

**症状**：

- 429 错误（请求过多）
- 配额用尽提示
- 间歇性失败

**解决方案**：

```typescript
class RateLimiter {
  private requests: number[] = [];
  private maxRequests = 60;
  private timeWindow = 60000; // 1分钟

  async waitIfNeeded(): Promise<void> {
    const now = Date.now();

    // 清理过期记录
    this.requests = this.requests.filter(
      (time) => now - time < this.timeWindow
    );

    // 检查是否超限
    if (this.requests.length >= this.maxRequests) {
      const oldestRequest = this.requests[0];
      const waitTime = this.timeWindow - (now - oldestRequest);

      console.log(`达到限流，等待 ${waitTime}ms`);
      await this.sleep(waitTime);
    }

    this.requests.push(now);
  }

  private sleep(ms: number): Promise<void> {
    return new Promise((resolve) => setTimeout(resolve, ms));
  }
}

// 使用示例
class ThrottledAgent extends AgentInstance {
  private rateLimiter = new RateLimiter();

  async process(input: string): Promise<string> {
    await this.rateLimiter.waitIfNeeded();
    return await super.process(input);
  }
}
```

### 调试技巧

#### 1. 启用详细日志

```typescript
class Logger {
  private level: "debug" | "info" | "warn" | "error" = "info";

  debug(message: string, data?: any): void {
    if (this.level === "debug") {
      console.log(`[DEBUG] ${message}`, data || "");
    }
  }

  logAgentRequest(agent: Agent, input: string): void {
    this.debug("Agent Request", {
      agentId: agent.id,
      agentName: agent.name,
      model: agent.model,
      temperature: agent.temperature,
      inputLength: input.length,
      timestamp: new Date().toISOString(),
    });
  }

  logAgentResponse(response: string, duration: number): void {
    this.debug("Agent Response", {
      responseLength: response.length,
      duration: `${duration}ms`,
      timestamp: new Date().toISOString(),
    });
  }
}

// 使用
const logger = new Logger();

async function processWithLogging(agent: AgentInstance, input: string) {
  logger.logAgentRequest(agent.agent, input);

  const startTime = Date.now();
  const response = await agent.process(input);
  const duration = Date.now() - startTime;

  logger.logAgentResponse(response, duration);

  return response;
}
```

#### 2. 性能监控

```typescript
class PerformanceMonitor {
  private metrics: Map<string, Metric[]> = new Map();

  record(agentId: string, metric: Metric): void {
    if (!this.metrics.has(agentId)) {
      this.metrics.set(agentId, []);
    }
    this.metrics.get(agentId)!.push(metric);
  }

  getStats(agentId: string): Stats {
    const metrics = this.metrics.get(agentId) || [];
    const durations = metrics.map((m) => m.duration);

    return {
      totalRequests: metrics.length,
      avgDuration: this.average(durations),
      minDuration: Math.min(...durations),
      maxDuration: Math.max(...durations),
      totalTokens: metrics.reduce((sum, m) => sum + m.tokens, 0),
    };
  }

  private average(numbers: number[]): number {
    return numbers.reduce((a, b) => a + b, 0) / numbers.length;
  }

  // 生成报告
  generateReport(): string {
    let report = "# Agent 性能报告\n\n";

    for (const [agentId, metrics] of this.metrics) {
      const stats = this.getStats(agentId);
      report += `## Agent: ${agentId}\n`;
      report += `- 总请求数: ${stats.totalRequests}\n`;
      report += `- 平均响应时间: ${stats.avgDuration.toFixed(2)}ms\n`;
      report += `- 总消耗 Token: ${stats.totalTokens}\n\n`;
    }

    return report;
  }
}

// 使用
const monitor = new PerformanceMonitor();

async function monitoredProcess(agent: AgentInstance, input: string) {
  const startTime = Date.now();
  const response = await agent.process(input);
  const duration = Date.now() - startTime;

  monitor.record(agent.agent.id, {
    duration,
    tokens: estimateTokens(input + response),
    timestamp: Date.now(),
  });

  return response;
}
```

#### 3. 测试工具

```typescript
class AgentTester {
  async testAgent(agent: Agent, testCases: TestCase[]): Promise<TestResult[]> {
    const results: TestResult[] = [];

    for (const testCase of testCases) {
      const instance = new AgentInstance(agent, this.model);
      const startTime = Date.now();

      try {
        const response = await instance.process(testCase.input);
        const duration = Date.now() - startTime;

        results.push({
          testCase: testCase.name,
          passed: this.validateResponse(response, testCase.expected),
          response,
          duration,
          error: null,
        });
      } catch (error) {
        results.push({
          testCase: testCase.name,
          passed: false,
          response: "",
          duration: Date.now() - startTime,
          error: error.message,
        });
      }
    }

    return results;
  }

  private validateResponse(response: string, expected: any): boolean {
    if (typeof expected === "function") {
      return expected(response);
    }
    if (expected instanceof RegExp) {
      return expected.test(response);
    }
    return response.includes(expected);
  }

  // 生成测试报告
  generateTestReport(results: TestResult[]): string {
    const passed = results.filter((r) => r.passed).length;
    const total = results.length;
    const passRate = ((passed / total) * 100).toFixed(2);

    let report = `# 测试报告\n\n`;
    report += `通过率: ${passRate}% (${passed}/${total})\n\n`;

    for (const result of results) {
      const status = result.passed ? "✅" : "❌";
      report += `${status} ${result.testCase} (${result.duration}ms)\n`;
      if (!result.passed && result.error) {
        report += `   错误: ${result.error}\n`;
      }
    }

    return report;
  }
}
```

### 错误处理最佳实践

```typescript
class RobustAgent extends AgentInstance {
  private maxRetries = 3;
  private retryDelay = 1000;

  async process(input: string): Promise<string> {
    for (let attempt = 1; attempt <= this.maxRetries; attempt++) {
      try {
        return await super.process(input);
      } catch (error) {
        console.error(`尝试 ${attempt}/${this.maxRetries} 失败:`, error);

        if (attempt === this.maxRetries) {
          throw new Error(
            `处理失败，已重试 ${this.maxRetries} 次: ${error.message}`
          );
        }

        // 指数退避
        await this.sleep(this.retryDelay * Math.pow(2, attempt - 1));
      }
    }

    throw new Error("不应该到达这里");
  }

  private sleep(ms: number): Promise<void> {
    return new Promise((resolve) => setTimeout(resolve, ms));
  }
}
```

## 更新日志

### v3.0.0 (2025-01-15)

**重大更新**

- 🎉 重构 Agent 架构，支持插件系统
- 🚀 新增 Agent 市场，社区共享
- 💡 智能推荐：根据任务自动推荐 Agent
- 🔧 支持 Agent 组合和工作流
- 📊 新增使用分析和性能监控

**新增 Agent**

- DevOps 工程师
- 安全专家
- 教育导师
- 内容创作者

**改进**

- 优化系统提示词模板
- 提升响应速度 40%
- 减少 Token 消耗 25%
- 增强错误处理机制

**修复**

- 修复长对话上下文丢失问题
- 修复工具调用超时
- 修复多语言配置加载错误

### v2.5.0 (2024-12-01)

**新功能**

- ✨ 支持自定义 Agent 模板
- 🎨 Agent 头像自定义（支持 Emoji 和图片）
- 📱 移动端 Agent 管理界面
- 🔄 Agent 配置同步（云端备份）

**优化**

- 改进 Agent 搜索和过滤
- 优化内存使用
- 提升加载速度

**修复**

- 修复 Agent 克隆功能问题
- 修复温度参数验证
- 修复导入导出编码问题

### v2.1.0 (2024-10-15)

**新增**

- 新增数据分析师 Agent
- 新增 UI/UX 设计师 Agent
- 支持 Agent 标签分类

**优化**

- 优化翻译专家提示词
- 改进文档撰写 Agent 输出格式
- 增强编程助手代码审查能力

**修复**

- 修复配置加载顺序问题
- 修复 Agent 参数验证
- 修复工具权限检查

### v2.0.0 (2024-08-01)

**重大更新**

- 🔄 重构 Agent 架构
- ✨ 支持完全自定义 Agent
- 🛠️ 新增工具集成功能
- 📦 统一配置文件格式

**新增 Agent**

- 编程助手
- 文档撰写
- 产品经理
- 翻译专家

**功能**

- Agent 分类和标签
- 批量导入导出
- 版本管理
- 使用统计

### v1.5.0 (2024-06-01)

**首次发布**

- 🎉 初始 Agent 系统
- 📝 基础编程助手
- 📄 文档撰写功能
- 🔧 配置管理

## 高级特性

### Agent 工作流

将多个 Agent 组合成工作流，自动化复杂任务：

```typescript
interface AgentWorkflow {
  id: string;
  name: string;
  description: string;
  steps: WorkflowStep[];
}

interface WorkflowStep {
  agentId: string;
  input: string | ((context: any) => string);
  output?: string;
  condition?: (context: any) => boolean;
}

class WorkflowExecutor {
  async execute(workflow: AgentWorkflow, initialInput: string): Promise<any> {
    const context = { input: initialInput, results: [] };

    for (const step of workflow.steps) {
      // 检查条件
      if (step.condition && !step.condition(context)) {
        continue;
      }

      // 准备输入
      const input =
        typeof step.input === "function" ? step.input(context) : step.input;

      // 执行 Agent
      const agent = agentManager.getAgent(step.agentId);
      const instance = new AgentInstance(agent, model);
      const result = await instance.process(input);

      // 保存结果
      context.results.push({ step: step.agentId, result });
    }

    return context.results;
  }
}

// 示例：完整的功能开发工作流
const featureDevelopmentWorkflow: AgentWorkflow = {
  id: "feature-dev",
  name: "功能开发工作流",
  description: "从需求到部署的完整流程",
  steps: [
    {
      agentId: "product-manager",
      input: (ctx) => `分析以下需求并生成 PRD：${ctx.input}`,
    },
    {
      agentId: "programming-assistant",
      input: (ctx) => `根据 PRD 设计技术方案：${ctx.results[0].result}`,
    },
    {
      agentId: "programming-assistant",
      input: (ctx) => `实现以下功能：${ctx.results[1].result}`,
    },
    {
      agentId: "security-expert",
      input: (ctx) => `审查以下代码的安全性：${ctx.results[2].result}`,
    },
    {
      agentId: "documentation-writer",
      input: (ctx) => `为以下功能编写文档：${ctx.results[2].result}`,
    },
    {
      agentId: "devops-engineer",
      input: (ctx) => `创建部署配置：${ctx.results[2].result}`,
    },
  ],
};
```

### Agent 插件系统

扩展 Agent 功能：

````typescript
interface AgentPlugin {
  name: string;
  version: string;
  hooks: {
    beforeProcess?: (input: string) => string;
    afterProcess?: (output: string) => string;
    onError?: (error: Error) => void;
  };
}

class PluginableAgent extends AgentInstance {
  private plugins: AgentPlugin[] = [];

  registerPlugin(plugin: AgentPlugin): void {
    this.plugins.push(plugin);
  }

  async process(input: string): Promise<string> {
    try {
      // 前置钩子
      let processedInput = input;
      for (const plugin of this.plugins) {
        if (plugin.hooks.beforeProcess) {
          processedInput = plugin.hooks.beforeProcess(processedInput);
        }
      }

      // 处理
      let output = await super.process(processedInput);

      // 后置钩子
      for (const plugin of this.plugins) {
        if (plugin.hooks.afterProcess) {
          output = plugin.hooks.afterProcess(output);
        }
      }

      return output;
    } catch (error) {
      // 错误钩子
      for (const plugin of this.plugins) {
        if (plugin.hooks.onError) {
          plugin.hooks.onError(error as Error);
        }
      }
      throw error;
    }
  }
}

// 插件示例：代码格式化
const codeFormatterPlugin: AgentPlugin = {
  name: "code-formatter",
  version: "1.0.0",
  hooks: {
    afterProcess: (output: string) => {
      // 提取代码块并格式化
      return output.replace(/```(\w+)\n([\s\S]*?)```/g, (match, lang, code) => {
        const formatted = formatCode(code, lang);
        return `\`\`\`${lang}\n${formatted}\`\`\``;
      });
    },
  },
};

// 插件示例：输入验证
const inputValidatorPlugin: AgentPlugin = {
  name: "input-validator",
  version: "1.0.0",
  hooks: {
    beforeProcess: (input: string) => {
      // 清理输入
      return input
        .trim()
        .replace(/<script>/gi, "") // 移除潜在的脚本
        .slice(0, 10000); // 限制长度
    },
  },
};
````

### Agent 市场

分享和发现 Agent：

```typescript
interface AgentMarketplace {
  search(query: string, filters?: MarketplaceFilters): Promise<AgentListing[]>;
  publish(agent: Agent): Promise<void>;
  install(agentId: string): Promise<Agent>;
  rate(agentId: string, rating: number): Promise<void>;
  getPopular(limit: number): Promise<AgentListing[]>;
}

interface AgentListing {
  agent: Agent;
  author: string;
  downloads: number;
  rating: number;
  reviews: Review[];
  createdAt: string;
  updatedAt: string;
}

interface MarketplaceFilters {
  category?: string;
  tags?: string[];
  minRating?: number;
  language?: string;
}

// 使用示例
const marketplace = new AgentMarketplace();

// 搜索 Agent
const agents = await marketplace.search("blockchain", {
  tags: ["solidity", "web3"],
  minRating: 4.0,
});

// 安装 Agent
const installedAgent = await marketplace.install("blockchain-expert-pro");

// 评分
await marketplace.rate("blockchain-expert-pro", 5);
```

### 智能推荐

根据任务自动推荐最适合的 Agent：

```typescript
class AgentRecommender {
  async recommend(task: string): Promise<Agent[]> {
    // 使用 AI 分析任务
    const analysis = await this.analyzeTask(task);

    // 匹配 Agent
    const allAgents = agentManager.getAllAgents();
    const scored = allAgents.map((agent) => ({
      agent,
      score: this.calculateScore(agent, analysis),
    }));

    // 排序并返回前 3 个
    return scored
      .sort((a, b) => b.score - a.score)
      .slice(0, 3)
      .map((item) => item.agent);
  }

  private async analyzeTask(task: string): Promise<TaskAnalysis> {
    // 提取关键词、意图、复杂度等
    return {
      keywords: this.extractKeywords(task),
      intent: await this.detectIntent(task),
      complexity: this.estimateComplexity(task),
      domain: this.identifyDomain(task),
    };
  }

  private calculateScore(agent: Agent, analysis: TaskAnalysis): number {
    let score = 0;

    // 标签匹配
    const tagMatch =
      agent.tags?.filter((tag) => analysis.keywords.includes(tag.toLowerCase()))
        .length || 0;
    score += tagMatch * 10;

    // 领域匹配
    if (agent.category === analysis.domain) {
      score += 20;
    }

    // 复杂度匹配
    const modelPower = this.getModelPower(agent.model);
    if (Math.abs(modelPower - analysis.complexity) < 2) {
      score += 15;
    }

    // 历史表现
    score += (agent.metadata?.rating || 0) * 5;

    return score;
  }

  private getModelPower(model: string): number {
    const powerMap: Record<string, number> = {
      "gpt-3.5-turbo": 3,
      "gpt-4": 5,
      "gpt-4-turbo": 7,
      "claude-3-haiku": 3,
      "claude-3-sonnet": 5,
      "claude-3-opus": 7,
    };
    return powerMap[model] || 5;
  }
}

// 使用示例
const recommender = new AgentRecommender();
const recommended = await recommender.recommend(
  "我需要优化一个 React 应用的性能，特别是首屏加载速度"
);

console.log(
  "推荐的 Agent:",
  recommended.map((a) => a.name)
);
// 输出: ['编程助手', 'UI/UX 设计师', 'DevOps 工程师']
```

### 多模态支持

支持图片、音频等多模态输入：

```typescript
interface MultiModalAgent extends Agent {
  supportedModalities: Modality[];
}

type Modality = "text" | "image" | "audio" | "video";

interface MultiModalInput {
  text?: string;
  images?: string[]; // URLs 或 base64
  audio?: string;
  video?: string;
}

class MultiModalAgentInstance extends AgentInstance {
  async processMultiModal(input: MultiModalInput): Promise<string> {
    // 处理多模态输入
    const messages = this.buildMultiModalMessages(input);

    const response = await this.model.chat({
      messages,
      // ... 其他参数
    });

    return response;
  }

  private buildMultiModalMessages(input: MultiModalInput): Message[] {
    const content: any[] = [];

    if (input.text) {
      content.push({ type: "text", text: input.text });
    }

    if (input.images) {
      input.images.forEach((image) => {
        content.push({ type: "image_url", image_url: { url: image } });
      });
    }

    return [
      { role: "system", content: this.agent.systemPrompt },
      { role: "user", content },
    ];
  }
}
```

## 贡献指南

我们欢迎社区贡献新的 Agent 或改进现有 Agent！

### 如何贡献

#### 1. 贡献新 Agent

**步骤**：

1. **Fork 项目**

   ```bash
   git clone https://github.com/yourusername/cherry-studio.git
   cd cherry-studio
   ```

2. **创建 Agent 配置**

   在 `resources/data/` 目录下创建或编辑 Agent 配置文件：

   ```json
   {
     "id": "your-agent-id",
     "name": "你的 Agent 名称",
     "description": "详细描述 Agent 的功能和用途",
     "avatar": "🤖",
     "model": "gpt-4",
     "systemPrompt": "精心设计的系统提示词...",
     "temperature": 0.5,
     "maxTokens": 2048,
     "tags": ["相关", "标签"],
     "category": "development"
   }
   ```

3. **编写测试用例**

   创建测试文件 `tests/agents/your-agent.test.ts`：

   ```typescript
   import { describe, it, expect } from "vitest";
   import { AgentManager } from "@/services/AgentManager";

   describe("Your Agent", () => {
     it("应该正确处理基本任务", async () => {
       const manager = new AgentManager();
       const agent = manager.getAgent("your-agent-id");
       const instance = new AgentInstance(agent, mockModel);

       const response = await instance.process("测试输入");
       expect(response).toContain("期望关键词");
     });
   });
   ```

4. **编写文档**

   在 `docs/agents/` 目录下创建 Agent 文档：

   ```markdown
   # Your Agent

   ## 简介

   简要介绍 Agent 的用途和特点

   ## 使用场景

   - 场景 1
   - 场景 2

   ## 示例

   ### 示例 1

   输入：...
   输出：...

   ## 配置说明

   - Temperature: 0.5（原因说明）
   - Model: GPT-4（原因说明）
   ```

5. **提交 Pull Request**

   ```bash
   git checkout -b feature/add-your-agent
   git add .
   git commit -m "feat: 添加 Your Agent"
   git push origin feature/add-your-agent
   ```

#### 2. 改进现有 Agent

**可以改进的方面**：

- 优化系统提示词
- 调整参数配置
- 添加新的使用示例
- 修复问题和 Bug
- 改进文档

**改进流程**：

1. 在 Issue 中描述问题或改进建议
2. 等待维护者确认
3. 实现改进并提交 PR
4. 参与代码审查

#### 3. 贡献文档

**文档类型**：

- 使用教程
- 最佳实践
- 常见问题解答
- 示例和案例

### 贡献标准

#### Agent 质量要求

✅ **必须满足**：

- [ ] 系统提示词清晰明确
- [ ] 包含完整的配置字段
- [ ] 提供至少 3 个测试用例
- [ ] 编写详细的文档
- [ ] 通过所有测试
- [ ] 遵循代码规范

✅ **推荐包含**：

- [ ] 使用示例和截图
- [ ] 常见问题解答
- [ ] 性能基准测试
- [ ] 与其他 Agent 的对比

#### 系统提示词规范

**好的提示词特征**：

- 🎯 明确定义角色和职责
- 📋 列出核心能力和知识领域
- 🔄 说明工作流程
- 📝 规定输出格式
- ⚠️ 明确限制和约束
- 🌟 体现专业性和特色

**示例对比**：

❌ **不好的提示词**：

```text
你是一个助手，帮助用户解决问题。
```

✅ **好的提示词**：

````text
你是一个资深的 Python 开发专家，拥有 10 年以上的全栈开发经验。

## 专业领域
- Python 3.x 核心特性和最佳实践
- Web 框架（Django, FastAPI, Flask）
- 异步编程和并发
- 测试驱动开发
- 性能优化和调试

## 工作方式
1. 仔细分析代码和需求
2. 提供 Pythonic 的解决方案
3. 解释设计决策和权衡
4. 包含完整的代码示例
5. 建议测试方法

## 代码标准
- 遵循 PEP 8 规范
- 使用类型注解
- 编写文档字符串
- 处理异常情况
- 优化性能

## 输出格式
- 代码使用 ```python``` 语法高亮
- 关键概念加粗显示
- 提供可运行的完整示例
````

#### 代码规范

**TypeScript/JavaScript**：

```typescript
// 使用有意义的变量名
const agentConfiguration: Agent = {
  id: "python-expert",
  name: "Python 专家",
  // ...
};

// 添加类型注解
function createAgent(config: Agent): AgentInstance {
  // ...
}

// 使用 JSDoc 注释
/**
 * 验证 Agent 配置
 * @param agent - Agent 配置对象
 * @returns 验证是否通过
 */
function validateAgent(agent: Agent): boolean {
  // ...
}
```

**JSON 配置**：

```json
{
  "id": "kebab-case-id",
  "name": "易读的名称",
  "description": "清晰完整的描述，说明用途和特点",
  "tags": ["排序的", "相关", "标签"]
}
```

### 审查流程

1. **自动检查**

   - ✅ 代码格式检查（ESLint, Prettier）
   - ✅ 类型检查（TypeScript）
   - ✅ 单元测试
   - ✅ 配置验证

2. **人工审查**

   - 📖 代码质量
   - 🎯 功能完整性
   - 📝 文档完善度
   - 🧪 测试覆盖率

3. **社区反馈**
   - 💬 讨论和建议
   - 🐛 Bug 报告
   - ⭐ 使用评价

### 测试指南

#### 单元测试

```typescript
describe("Agent Manager", () => {
  let manager: AgentManager;

  beforeEach(() => {
    manager = new AgentManager("./test-config.json");
  });

  it("应该加载 Agent 配置", () => {
    const agents = manager.getAllAgents();
    expect(agents.length).toBeGreaterThan(0);
  });

  it("应该验证无效配置", () => {
    const invalidAgent = { id: "test" };
    expect(() => manager.validateAgent(invalidAgent as Agent)).toThrow(
      "缺少必填字段"
    );
  });

  it("应该正确处理温度参数", () => {
    const agent = manager.getAgent("test-agent");
    expect(agent?.temperature).toBeGreaterThanOrEqual(0);
    expect(agent?.temperature).toBeLessThanOrEqual(2);
  });
});
```

#### 集成测试

```typescript
describe("Agent 集成测试", () => {
  it("应该能够完成完整对话", async () => {
    const agent = manager.getAgent("programming-assistant");
    const instance = new AgentInstance(agent, realModel);

    const response = await instance.process("用 TypeScript 实现一个单例模式");

    expect(response).toContain("class");
    expect(response).toContain("static");
    expect(response).toContain("instance");
  });

  it("应该保持对话上下文", async () => {
    const agent = manager.getAgent("programming-assistant");
    const instance = new AgentInstance(agent, realModel);

    await instance.process("我需要一个计数器类");
    const response = await instance.process("添加重置功能");

    // 应该理解"添加"指的是给之前的计数器类添加功能
    expect(response).toContain("reset");
  });
});
```

#### 性能测试

```typescript
describe("Agent 性能测试", () => {
  it("应该在合理时间内响应", async () => {
    const startTime = Date.now();
    const response = await instance.process("简单问题");
    const duration = Date.now() - startTime;

    expect(duration).toBeLessThan(5000); // 5秒内
  });

  it("应该高效使用 Token", async () => {
    const input = "写一个 Hello World 程序";
    const response = await instance.process(input);
    const tokens = estimateTokens(input + response);

    expect(tokens).toBeLessThan(500); // 简单任务应该控制在 500 tokens 内
  });
});
```

### 版本管理

遵循 [语义化版本](https://semver.org/lang/zh-CN/)：

- **主版本号**：不兼容的 API 修改
- **次版本号**：向下兼容的功能性新增
- **修订号**：向下兼容的问题修正

**示例**：

```json
{
  "metadata": {
    "version": "2.1.3",
    "changelog": [
      "2.1.3: 修复温度参数验证问题",
      "2.1.0: 新增代码解释器支持",
      "2.0.0: 重构系统提示词"
    ]
  }
}
```

### 获取帮助

- 📖 查看 [完整文档](CONTRIBUTING.md)
- 💬 加入 [Discord 社区](https://discord.gg/cherry-studio)
- 🐛 提交 [Issue](https://github.com/cherry-studio/cherry-studio/issues)
- 📧 邮件联系: contribute@cherry-studio.ai

### 贡献者名单

感谢所有贡献者！🎉

<!-- 贡献者列表会自动生成 -->

### 许可协议

通过贡献代码，你同意你的贡献将按照项目的 [MIT 许可证](LICENSE) 进行许可。

---

## 常见问题 (FAQ)

### 关于使用

**Q: 如何选择合适的 Agent？**

A: 根据任务类型选择：

- 写代码 → 编程助手
- 写文档 → 文档撰写
- 分析数据 → 数据分析师
- 设计产品 → 产品经理

不确定时可以使用智能推荐功能。

**Q: 可以同时使用多个 Agent 吗？**

A: 可以！建议使用工作流功能组合多个 Agent，每个 Agent 负责特定环节。

**Q: Agent 会记住之前的对话吗？**

A: 会的。每个 Agent 实例会保持对话历史，直到重置或达到上下文限制。

**Q: 如何让 Agent 输出更准确？**

A:

1. 提供详细的上下文
2. 明确说明期望结果
3. 必要时调低温度参数
4. 选择更强大的模型

### 关于配置

**Q: Temperature 参数如何设置？**

A:

- 0.0-0.3: 确定性任务（代码、翻译）
- 0.4-0.6: 平衡任务（技术文档）
- 0.7-1.0: 创造性任务（创作、设计）

**Q: 如何限制 Token 消耗？**

A:

1. 设置合理的 `maxTokens`
2. 精简系统提示词
3. 定期清理对话历史
4. 使用更小的模型

**Q: Agent 支持哪些模型？**

A: 支持所有兼容 OpenAI API 的模型，包括：

- GPT-3.5/4 系列
- Claude 系列
- 本地部署的开源模型

### 关于开发

**Q: 如何调试 Agent？**

A:

1. 启用详细日志
2. 使用测试工具
3. 查看性能监控数据
4. 使用小数据集测试

**Q: 如何优化 Agent 性能？**

A:

1. 优化系统提示词长度
2. 选择合适的模型
3. 实现缓存机制
4. 使用批处理

**Q: 如何分享我的 Agent？**

A:

1. 导出配置文件
2. 发布到 Agent 市场
3. 提交到官方仓库
4. 在社区分享

### 故障排除

**Q: Agent 响应很慢怎么办？**

A: 检查：

- 网络连接
- 模型负载
- Token 限制
- 提示词长度

**Q: Agent 输出格式错误？**

A:

1. 检查系统提示词中的格式要求
2. 使用示例来明确格式
3. 添加格式验证插件

**Q: 如何重置 Agent 状态？**

A:

```typescript
agentInstance.reset(); // 清除对话历史
```

---

## 资源链接

### 官方资源

- 📘 [官方文档](https://docs.cherry-studio.ai)
- 🏠 [官方网站](https://cherry-studio.ai)
- 📦 [GitHub 仓库](https://github.com/cherry-studio/cherry-studio)
- 🎨 [Agent 市场](https://agents.cherry-studio.ai)

### 社区

- 💬 [Discord 社区](https://discord.gg/cherry-studio)
- 🐦 [Twitter](https://twitter.com/cherry_studio)
- 📺 [YouTube 频道](https://youtube.com/@cherry-studio)
- 📝 [技术博客](https://blog.cherry-studio.ai)

### 教程和示例

- 📚 [入门教程](https://docs.cherry-studio.ai/getting-started)
- 🎓 [进阶指南](https://docs.cherry-studio.ai/advanced)
- 💡 [最佳实践](https://docs.cherry-studio.ai/best-practices)
- 🔧 [API 文档](https://docs.cherry-studio.ai/api)

### 开发工具

- 🛠️ [Agent 开发套件](https://github.com/cherry-studio/agent-sdk)
- 🧪 [测试工具](https://github.com/cherry-studio/agent-tester)
- 📊 [性能分析器](https://github.com/cherry-studio/agent-profiler)

---

## 许可证

本项目采用 [MIT 许可证](LICENSE)

```
MIT License

Copyright (c) 2024 Cherry Studio

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 致谢

感谢所有为 Cherry Studio Agent 系统做出贡献的开发者和用户！

特别感谢：

- OpenAI 提供强大的 AI 模型
- Anthropic Claude 团队
- 开源社区的支持和反馈

---

**Happy Coding! 🍒**
