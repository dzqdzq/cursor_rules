# Cursor Rules

Cursor IDE 的规则和配置文件集合，包含 React、Vue.js、ESLint 配置以及开发工作流程相关规则。

## 项目结构

```
cursor_rules/
├── command/          # 命令和工具使用说明
├── eslint/          # ESLint 配置文件
│   ├── cocos/       # Cocos Creator ESLint 配置
│   └── normal_js_proj/  # 普通 JavaScript 项目 ESLint 配置
├── rules/           # Cursor 规则文件
│   ├── react.mdc    # React 开发规则
│   └── vuejs.mdc    # Vue.js 开发规则
├── mcp.json         # MCP 服务器配置
└── README.md        # 项目说明
```

## 规则说明

### React 规则 (rules/react.mdc)
- 使用函数组件和 Hooks
- 使用自定义 Hooks 处理可复用逻辑
- 使用 Context API 进行状态管理
- 使用 PropTypes 进行属性验证
- 使用 React.memo 进行性能优化
- 使用 Fragment 避免不必要的 DOM 元素
- 使用正确的 key 进行列表渲染
- 优先使用组合而非继承

### Vue.js 规则 (rules/vuejs.mdc)
- 使用 Composition API 和 `<script setup>`
- 定义带类型和默认值的 props
- 使用 emits 处理组件事件
- 使用 v-model 进行双向绑定
- 使用 computed 处理派生状态
- 使用 watchers 处理副作用
- 使用 provide/inject 进行深层组件通信
- 使用异步组件进行代码分割

## 命令说明

### 文件格式化 (command/js文件格式化wakaru.md)
使用 wakaru CLI 工具格式化 JavaScript 文件：
```bash
npx --yes @wakaru/cli unminify {指定路径}/**/*.js
```

### 安全审计 (command/安全审计.md)
全面的安全审查流程，包括：
- 依赖项审计
- 代码安全审查
- 基础设施安全

### 需求确认 (command/需求确认.md)
在开始开发前，先与用户确认需求，确保理解正确。

## MCP 配置

`mcp.json` 文件包含以下 MCP 服务器配置：
- GitHub MCP 服务器
- MCP Feedback Enhanced
- Context7
- Playwright

## 使用方式

将这些规则文件放置在 Cursor IDE 的规则目录中，IDE 将自动应用这些规则来辅助开发。

## 许可证

MIT License
