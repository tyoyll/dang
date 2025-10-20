## React 2 个月系统学习计划（官方文档为主 + 练习与考题）

- **适用人群**: 有 Vue 基础的同学，转学/进阶 React
- **学习目标（2 个月）**
  - 掌握 React 核心理念：声明式 UI、组件化、单向数据流
  - 熟悉 JSX、事件、受控表单、列表与条件渲染
  - 系统掌握 Hooks：useState/useEffect/useRef/useMemo/useCallback/useReducer/useContext
  - 理解 Context、性能优化、代码拆分与懒加载、基础测试
  - 能用 Vite 搭建 React 工程，独立完成一个小中型页面/应用
- **主线资料（务必优先）**
  - React 官方学习路径（英文/中文）：`https://react.dev/learn`（[中文镜像](https://zh-hans.react.dev/learn)）
  - Hooks API 参考：`https://react.dev/reference/react`
  - TypeScript 与 React：`https://react.dev/learn/typescript`
  - 测试入门：`https://react.dev/learn/testing`

---

### 学习节奏建议
- 每周 5 天学习 + 2 天机动复盘
- 每天 60–120 分钟：阅读（40%）+ 练习（50%）+ 复盘（10%）
- 每周要有“可交付物”（小组件/小页面/小功能）

### Vue → React 快速对照
- 模板 vs JSX：Vue 用 `<template>` 与指令；React 用 JSX（JavaScript 即模板）
- 响应式 vs 显式状态：Vue 自动依赖跟踪；React 用 `useState` 明确更新
- 插槽 vs `children`：Vue 插槽强语义；React 用 `props.children` 组合
- provide/inject vs Context：跨层传递数据的两种机制
- 生命周期 vs Hooks：函数组件 + Hooks 表达组件“阶段”需求

---

## 第 1 周：入门与基石（JSX / 组件 / Props）
- 阅读（官方）：
  - Quick Start, Describing the UI
  - Conditional Rendering, Rendering Lists
- 实践任务：
  - 用 Vite 创建 React + TS 项目；配置 ESLint + Prettier
  - 写 3 个基础组件：`Avatar`、`Button`、`Card`（覆盖文本/布尔/对象型 props）
  - 用 JSX 渲染“联系人列表”（包含稳定 `key`）
- 练习题：
  1) 将一个静态 HTML 卡片改写为 React 组件，拆分头/身/尾
  2) 用 props 控制 `Button` 的样式（primary/ghost/disabled）
  3) 写 `List` 组件（接收数组与 `renderItem` 函数）
- 章节考题（自测）：
  - JSX 与 HTML 的 3 个关键差异？
  - 为什么列表渲染必须提供稳定的 `key`？
  - props 与 state 的职责边界在哪里？
  - 为什么组件应保持“纯”（pure）？

## 第 2 周：交互与状态（事件 / useState / 表单）
- 阅读（官方）：
  - Adding Interactivity, State: A Component’s Memory
  - Updating Objects/Arrays in State
- 实践任务：
  - 计数器（单步、多步、延时 + 函数式更新）
  - 受控表单：登录表单（输入校验、禁用提交、loading）
  - Todo 列表（新增/完成/过滤）
- 练习题：
  1) 将多输入表单状态合并成对象（不可变更新）
  2) 为列表项添加“内联编辑”模式切换
  3) 实现带搜索的下拉选择（受控组件）
- 章节考题（自测）：
  - 受控 vs 非受控组件的区别与场景？
  - 为什么推荐 `setState(prev => ...)` 函数式更新？
  - 更新数组/对象状态时为何必须保持不可变性？

## 第 3 周：组件关系（组合 / children / 状态提升）
- 阅读（官方）：
  - Passing Props to a Component, Keeping Components Pure
  - Sharing State Between Components
- 实践任务：
  - 构建 `<Tabs>` + `<TabPanel>`（用 `children` 复合组件模式）
  - “购物车”场景：商品列表 + 购物车（将状态提升到共同父级）
- 练习题：
  1) 将筛选栏条件从子组件提升到父组件集中管理
  2) 编写“受控模态框”（父组件控制显示与关闭）
  3) 练习 `children` + 复合组件（如 `<Form.Item>` 风格）
- 章节考题（自测）：
  - 何时应“提升状态”？提升后的利弊？
  - `children` 与 Vue 插槽的差异？
  - 解释“自顶向下的单向数据流”的优势。

## 第 4 周：跨层通信与复杂状态（Context / useReducer / 自定义 Hooks）
- 阅读（官方）：
  - Passing Data Deeply with Context, useContext, useReducer
  - Reusing Logic with Custom Hooks
- 实践任务：
  - 主题/语言上下文切换（全局主题）
  - 通知中心：用 `useReducer` 管理消息队列（增/删/已读）
  - 抽象常用 Hook：`useToggle`、`usePagination`
- 练习题：
  1) 用 Context 提供用户信息，任意子组件消费
  2) 用 `useReducer` 重写 Todo（拆分 action 常量）
  3) 将“列表 + 分页 + 加载”的逻辑抽到 `useListData`
- 章节考题（自测）：
  - Context 的使用边界与不适用场景？
  - `useReducer` 相比 `useState` 的优势场景？
  - 设计一个自定义 Hook 的输入/输出 API（无需代码）。

## 第 5 周：副作用与数据同步（useEffect / useRef）
- 阅读（官方）：
  - Synchronizing with Effects, You Might Not Need an Effect
  - Referencing Values with Refs, useEffect/useRef API
- 实践任务：
  - 数据面板：加载、错误、重试、取消（AbortController）
  - `ref` 控制 DOM（滚动到视图、聚焦）
  - 对比“应该避免的 Effect”与“必要的 Effect”并重构
- 练习题：
  1) “搜索框 + 远程搜索”（避免竞态，旧请求作废）
  2) 用 `ref` 记录上一次 props 值，打印“变化日志”
  3) 将不必要的 Effect 重构为派生状态或事件处理
- 章节考题（自测）：
  - 列举 3 种“不需要 Effect”的典型情形
  - 解释依赖数组与闭包陷阱
  - `ref` 与 state 的区别？更新 `ref.current` 是否触发渲染？

## 第 6 周：项目结构、路由与 TypeScript（补充）
- 阅读（官方主线仍为 React 文档）：
  - TypeScript in React
- 补充（常用但非官方）：
  - React Router 文档：`https://reactrouter.com`
- 实践任务：
  - Vite + React + TS + React Router 搭建多页面小站（首页/列表/详情/关于）
  - 目录模块化：`features/`、`components/`、`hooks/`、`pages/`
- 练习题：
  1) 用 TS 为组件 props 建模（必填/可选、联合、回调）
  2) 封装 `useQueryParams`（读写 URL 查询参数）
  3) 路由懒加载 + 布局组件（导航 + 内容区）
- 章节考题（自测）：
  - 如何在现有项目中逐步引入 TS？
  - 设计 `UserCard` 的 props 类型（只需类型定义）。

## 第 7 周：性能优化与体验（memo/useMemo/useCallback、lazy/Suspense）
- 阅读（官方）：
  - Escape Hatches（Memoizing），useMemo/useCallback/memo
  - lazy 与 Suspense，过渡更新 useTransition/useDeferredValue
- 实践任务：
  - 为列表/表单添加 `React.memo` 与回调缓存，分析重渲染
  - 用 `lazy` + `Suspense` 拆分路由或大组件
  - 大列表虚拟化（可选：react-window）
- 练习题：
  1) 比较“无优化 vs memo/useMemo/useCallback”的渲染性能
  2) 为搜索输入加入 `useDeferredValue`，保持输入流畅
  3) 用 `useTransition` 做“切换视图”的柔顺过渡
- 章节考题（自测）：
  - 何时不应使用 `useMemo`/`useCallback`？
  - `Suspense` 的作用？与路由懒加载如何配合？
  - 举例一次“不必要的重渲染”与应对策略。

## 第 8 周：综合实战与验收
- 小项目建议（选一或自拟）：
  - 任务看板（拖拽/过滤/详情侧栏）
  - 书签管理器（标签、搜索、批量、详情）
  - 课程表/日程（日/周视图、增删改、提醒）
- 要求：
  - Vite + React + TS；≥ 6–8 个可复用组件
  - 路由 + 懒加载；表单（校验 + 受控）；远程数据（加载/错误/重试）
  - 基本性能优化（memo/回调缓存/代码拆分）
  - 测试 3–5 个关键逻辑/组件
- 验收清单：
  - 组件树与数据流是否清晰？
  - 关键状态是否合理拆分（本地/UI/服务器状态）？
  - Effect 是否仅用于必要的副作用？
  - 是否存在不必要重渲染？
  - 是否有基本单测/集成测试？

---

### 每章结束统一“考题模板”（复用）
- 用自己的话解释本章 3–5 个核心概念
- 找出项目中可改进之处并动手重构
- 列出 2 个“易混点/常犯错”与避免策略
- 用 3–5 句话总结“最佳实践”

### 每日微练习（任选）
- 用 JSX 重写一个小 HTML 片段（10 分钟）
- 将一个状态从子组件提升到父组件（15 分钟）
- 把重复逻辑抽成自定义 Hook（15 分钟）
- 给组件加上 TS 类型（10 分钟）
- 用 `lazy` 拆分一个路由（10 分钟）

---

### 工具与环境建议
- Node.js 18+；包管理器（pnpm/npm 任一）
- 构建：Vite（`pnpm create vite` 选择 React + TS）
- 质量：ESLint + Prettier；可选 UI 库：Ant Design / MUI

### 资源速查（官方为主）
- React Learn：`https://react.dev/learn`
- Hooks 参考：`https://react.dev/reference/react`
- TypeScript：`https://react.dev/learn/typescript`
- Testing：`https://react.dev/learn/testing`
- React Router（补充）：`https://reactrouter.com`

---

最后更新：2025-10-20  ·  目标版本：React 18.x
