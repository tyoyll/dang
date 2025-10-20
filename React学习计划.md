# React 学习计划（2个月）

## 📚 学习目标
通过2个月的系统学习，掌握React的核心概念和实战技能，能够独立搭建React Web应用。

## ⏰ 学习安排
- **总时长**: 2个月（8周）
- **每日学习时间**: 1小时
- **总学习时间**: 约60小时

## 🎯 前置说明
由于你已有Vue基础，以下概念会帮助你快速理解React：

### Vue vs React 核心差异对比

| 特性 | Vue | React |
|-----|-----|-------|
| 数据绑定 | 双向绑定 (v-model) | 单向数据流 |
| 模板语法 | Template | JSX |
| 组件定义 | SFC (.vue文件) | 函数组件/类组件 |
| 状态管理 | data/computed | useState/useReducer |
| 生命周期 | mounted/updated等 | useEffect |
| 条件渲染 | v-if/v-show | 条件表达式/&& |
| 列表渲染 | v-for | map() |

---

## 📅 第一阶段：React基础概念（第1-2周）

### 第1周：React入门与环境搭建

#### Day 1-2: React简介与开发环境
**学习内容：**
- React的历史和设计理念
- 为什么选择React（与Vue对比）
- 搭建开发环境
  - Node.js和npm/yarn安装
  - 使用Create React App创建项目
  - 了解项目结构

**学习资源：**
- 📖 [React官方文档 - 快速入门](https://zh-hans.react.dev/learn)
- 🎥 推荐视频：[React入门教程 - 程序员峰峰](https://www.bilibili.com/video/BV1wy4y1D7JT)

**练习题：**
1. 创建你的第一个React应用，显示"Hello React!"
2. 修改App.js，添加你的个人信息展示
3. 尝试修改CSS样式，美化页面

```jsx
// 练习示例代码
function App() {
  // TODO: 在这里添加你的代码
  return (
    <div className="App">
      <h1>Hello React!</h1>
      {/* 添加更多内容 */}
    </div>
  );
}
```

#### Day 3-4: JSX语法与组件基础
**学习内容：**
- JSX语法详解
  - JSX表达式
  - 条件渲染
  - 列表渲染
- 函数组件vs类组件（重点学习函数组件）
- Props传递数据

**学习资源：**
- 📖 [React官方文档 - JSX简介](https://zh-hans.react.dev/learn/writing-markup-with-jsx)
- 📖 [React官方文档 - 组件与Props](https://zh-hans.react.dev/learn/your-first-component)

**练习题：**
1. 创建一个用户卡片组件，接收name、age、avatar等props
2. 实现一个商品列表，使用map渲染多个商品
3. 添加条件渲染，根据库存显示不同状态

```jsx
// 练习示例：用户卡片组件
function UserCard({ name, age, avatar }) {
  // TODO: 实现用户卡片
  return (
    <div className="user-card">
      {/* 你的代码 */}
    </div>
  );
}

// 练习示例：商品列表
function ProductList() {
  const products = [
    { id: 1, name: '商品1', price: 99, stock: 10 },
    { id: 2, name: '商品2', price: 199, stock: 0 },
    // ...
  ];
  
  // TODO: 使用map渲染商品列表
  return (
    <div>
      {/* 你的代码 */}
    </div>
  );
}
```

#### Day 5-7: 事件处理与状态管理入门
**学习内容：**
- 事件处理机制
- useState Hook入门
- 状态提升
- 受控组件与非受控组件

**学习资源：**
- 📖 [React官方文档 - 响应事件](https://zh-hans.react.dev/learn/responding-to-events)
- 📖 [React官方文档 - State: 组件的记忆](https://zh-hans.react.dev/learn/state-a-components-memory)
- 🎥 推荐视频：[React Hooks详解](https://www.bilibili.com/video/BV1Ma411h7L6)

**练习题：**
1. 创建一个计数器组件（增加、减少、重置）
2. 实现一个Todo列表（添加、删除、标记完成）
3. 创建一个表单组件（姓名、邮箱、提交）

```jsx
// 练习示例：计数器组件
import { useState } from 'react';

function Counter() {
  // TODO: 使用useState管理计数
  const [count, setCount] = useState(0);
  
  // TODO: 实现增加、减少、重置功能
  return (
    <div>
      <h2>计数器: {count}</h2>
      {/* 添加按钮 */}
    </div>
  );
}
```

### 第2周：深入理解React核心概念

#### Day 8-10: 组件生命周期与useEffect
**学习内容：**
- useEffect Hook详解
- 副作用处理
- 清理函数
- 依赖数组的使用

**学习资源：**
- 📖 [React官方文档 - Effect Hook](https://zh-hans.react.dev/learn/synchronizing-with-effects)
- 📖 [React官方文档 - 你可能不需要Effect](https://zh-hans.react.dev/learn/you-might-not-need-an-effect)

**练习题：**
1. 创建一个时钟组件，每秒更新时间
2. 实现数据获取组件（模拟API调用）
3. 创建一个窗口大小监听组件

```jsx
// 练习示例：时钟组件
import { useState, useEffect } from 'react';

function Clock() {
  const [time, setTime] = useState(new Date());
  
  useEffect(() => {
    // TODO: 设置定时器更新时间
    // TODO: 清理定时器
  }, []);
  
  return <div>{/* 显示时间 */}</div>;
}
```

#### Day 11-14: 组件通信进阶
**学习内容：**
- Props深入理解
- Children属性
- 组件组合vs继承
- Context API基础

**学习资源：**
- 📖 [React官方文档 - 组件间传递数据](https://zh-hans.react.dev/learn/passing-props-to-a-component)
- 📖 [React官方文档 - Context深入](https://zh-hans.react.dev/learn/passing-data-deeply-with-context)

**练习题：**
1. 创建一个主题切换系统（使用Context）
2. 实现一个购物车组件（父子组件通信）
3. 创建一个模态框组件（使用children）

### 📝 第一阶段测验题

1. **概念理解题**
   - 什么是JSX？它与HTML有什么区别？
   - React中的单向数据流是什么意思？
   - 函数组件和类组件的主要区别是什么？

2. **代码分析题**
   ```jsx
   function App() {
     const [count, setCount] = useState(0);
     
     const handleClick = () => {
       setCount(count + 1);
       setCount(count + 1);
     };
     
     return <button onClick={handleClick}>{count}</button>;
   }
   ```
   问题：点击按钮后，count的值是多少？为什么？

3. **实践题**
   创建一个简单的用户管理系统，包含：
   - 用户列表展示
   - 添加新用户
   - 删除用户
   - 编辑用户信息

---

## 📅 第二阶段：组件深入与状态管理（第3-4周）

### 第3周：高级组件模式

#### Day 15-17: 自定义Hooks
**学习内容：**
- 什么是自定义Hooks
- 创建和使用自定义Hooks
- Hooks规则和最佳实践
- 常用自定义Hooks模式

**学习资源：**
- 📖 [React官方文档 - 自定义Hook](https://zh-hans.react.dev/learn/reusing-logic-with-custom-hooks)
- 🎥 推荐视频：[自定义Hooks实战](https://www.bilibili.com/video/BV1iV411b7L1)

**练习题：**
1. 创建useLocalStorage Hook（本地存储）
2. 创建useFetch Hook（数据获取）
3. 创建useDebounce Hook（防抖）

```jsx
// 练习示例：useLocalStorage Hook
function useLocalStorage(key, initialValue) {
  // TODO: 实现本地存储逻辑
  const [value, setValue] = useState(() => {
    // 从localStorage读取初始值
  });
  
  // TODO: 监听value变化，同步到localStorage
  
  return [value, setValue];
}

// 使用示例
function App() {
  const [name, setName] = useLocalStorage('userName', '');
  // ...
}
```

#### Day 18-21: 性能优化
**学习内容：**
- React.memo
- useMemo和useCallback
- 懒加载和代码分割
- 虚拟化长列表

**学习资源：**
- 📖 [React官方文档 - 性能优化](https://zh-hans.react.dev/learn/render-and-commit)
- 📖 [React官方文档 - useMemo](https://zh-hans.react.dev/reference/react/useMemo)

**练习题：**
1. 优化一个大列表渲染性能
2. 实现图片懒加载组件
3. 使用React.memo优化子组件渲染

```jsx
// 练习示例：优化列表渲染
import { memo, useMemo } from 'react';

const ExpensiveList = memo(({ items, filter }) => {
  // TODO: 使用useMemo优化过滤逻辑
  const filteredItems = useMemo(() => {
    // 过滤逻辑
  }, [items, filter]);
  
  return (
    <ul>
      {/* 渲染列表 */}
    </ul>
  );
});
```

### 第4周：表单处理与验证

#### Day 22-24: 复杂表单处理
**学习内容：**
- 受控组件深入
- 表单验证策略
- 第三方表单库（React Hook Form）
- 文件上传处理

**学习资源：**
- 📖 [React官方文档 - 表单](https://zh-hans.react.dev/learn/reacting-to-input-with-state)
- 📖 [React Hook Form文档](https://react-hook-form.com/get-started)

**练习题：**
1. 创建一个注册表单（包含验证）
2. 实现动态表单字段
3. 创建一个多步骤表单

```jsx
// 练习示例：注册表单
function RegistrationForm() {
  const [formData, setFormData] = useState({
    username: '',
    email: '',
    password: '',
    confirmPassword: ''
  });
  
  const [errors, setErrors] = useState({});
  
  // TODO: 实现表单验证逻辑
  const validateForm = () => {
    // 验证规则
  };
  
  // TODO: 处理表单提交
  const handleSubmit = (e) => {
    e.preventDefault();
    // 提交逻辑
  };
  
  return (
    <form onSubmit={handleSubmit}>
      {/* 表单字段 */}
    </form>
  );
}
```

#### Day 25-28: 状态管理进阶
**学习内容：**
- useReducer Hook
- Context + useReducer模式
- 状态管理库介绍（Redux Toolkit、Zustand）
- 全局状态vs局部状态

**学习资源：**
- 📖 [React官方文档 - useReducer](https://zh-hans.react.dev/reference/react/useReducer)
- 📖 [Redux Toolkit官方文档](https://redux-toolkit.js.org/introduction/getting-started)
- 🎥 推荐视频：[Redux Toolkit教程](https://www.bilibili.com/video/BV1MG411K7Wm)

**练习题：**
1. 使用useReducer重构Todo应用
2. 创建一个购物车状态管理
3. 实现用户认证状态管理

### 📝 第二阶段测验题

1. **概念理解题**
   - 什么时候应该使用useMemo和useCallback？
   - 自定义Hook的命名规则是什么？为什么？
   - useReducer vs useState，如何选择？

2. **性能优化题**
   分析以下代码的性能问题并优化：
   ```jsx
   function ParentComponent() {
     const [count, setCount] = useState(0);
     const [text, setText] = useState('');
     
     const expensiveValue = calculateExpensive(count);
     
     return (
       <>
         <ChildComponent value={expensiveValue} />
         <input value={text} onChange={e => setText(e.target.value)} />
       </>
     );
   }
   ```

3. **实践题**
   创建一个完整的表单应用，包含：
   - 多种输入类型（文本、选择、复选框等）
   - 实时验证
   - 错误提示
   - 提交前验证

---

## 📅 第三阶段：路由与数据获取（第5-6周）

### 第5周：React Router

#### Day 29-31: 路由基础
**学习内容：**
- React Router安装与配置
- 基础路由设置
- 嵌套路由
- 路由参数和查询字符串

**学习资源：**
- 📖 [React Router官方文档](https://reactrouter.com/en/main/start/tutorial)
- 🎥 推荐视频：[React Router v6教程](https://www.bilibili.com/video/BV1EM4y1Q7wg)

**练习题：**
1. 创建一个多页面应用（首页、关于、联系我们）
2. 实现产品详情页（动态路由）
3. 创建一个带有嵌套路由的管理后台

```jsx
// 练习示例：路由配置
import { BrowserRouter, Routes, Route, Link } from 'react-router-dom';

function App() {
  return (
    <BrowserRouter>
      <nav>
        <Link to="/">首页</Link>
        <Link to="/about">关于</Link>
        <Link to="/products">产品</Link>
      </nav>
      
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/products" element={<Products />}>
          <Route path=":id" element={<ProductDetail />} />
        </Route>
      </Routes>
    </BrowserRouter>
  );
}
```

#### Day 32-35: 路由进阶
**学习内容：**
- 路由守卫（Protected Routes）
- 路由懒加载
- 路由动画
- 编程式导航

**学习资源：**
- 📖 [React Router高级指南](https://reactrouter.com/en/main/start/concepts)

**练习题：**
1. 实现登录认证路由守卫
2. 添加路由切换动画
3. 创建面包屑导航组件

```jsx
// 练习示例：路由守卫
function ProtectedRoute({ children }) {
  const isAuthenticated = useAuth(); // 自定义Hook
  
  if (!isAuthenticated) {
    return <Navigate to="/login" />;
  }
  
  return children;
}

// 使用
<Route path="/admin" element={
  <ProtectedRoute>
    <AdminPanel />
  </ProtectedRoute>
} />
```

### 第6周：数据获取与状态同步

#### Day 36-38: 数据获取策略
**学习内容：**
- Fetch API和Axios
- 加载状态处理
- 错误处理
- 数据缓存策略

**学习资源：**
- 📖 [React官方文档 - 获取数据](https://zh-hans.react.dev/learn/synchronizing-with-effects#fetching-data)
- 📖 [Axios文档](https://axios-http.com/zh/docs/intro)

**练习题：**
1. 创建一个新闻列表（带分页）
2. 实现搜索功能（带防抖）
3. 创建数据刷新机制

```jsx
// 练习示例：数据获取Hook
function useFetch(url) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);
  
  useEffect(() => {
    const fetchData = async () => {
      try {
        setLoading(true);
        const response = await fetch(url);
        const data = await response.json();
        setData(data);
      } catch (err) {
        setError(err);
      } finally {
        setLoading(false);
      }
    };
    
    fetchData();
  }, [url]);
  
  return { data, loading, error };
}
```

#### Day 39-42: 数据管理库
**学习内容：**
- React Query/TanStack Query
- SWR简介
- 乐观更新
- 缓存失效策略

**学习资源：**
- 📖 [TanStack Query文档](https://tanstack.com/query/latest/docs/react/overview)
- 🎥 推荐视频：[React Query实战](https://www.bilibili.com/video/BV1Kr4y1s7kv)

**练习题：**
1. 使用React Query重构数据获取
2. 实现乐观更新（点赞功能）
3. 创建实时数据同步

### 📝 第三阶段测验题

1. **路由理解题**
   - React Router v6与v5的主要区别？
   - 如何实现路由级别的代码分割？
   - 什么是路由守卫？如何实现？

2. **数据获取题**
   优化以下数据获取代码：
   ```jsx
   function UserProfile({ userId }) {
     const [user, setUser] = useState(null);
     
     useEffect(() => {
       fetch(`/api/users/${userId}`)
         .then(res => res.json())
         .then(data => setUser(data));
     }, []);
     
     return <div>{user?.name}</div>;
   }
   ```

3. **综合实践题**
   创建一个博客应用，包含：
   - 文章列表页
   - 文章详情页
   - 分类筛选
   - 搜索功能
   - 分页加载

---

## 📅 第四阶段：生态系统与项目实战（第7-8周）

### 第7周：UI库与工具链

#### Day 43-45: UI组件库
**学习内容：**
- Ant Design使用
- Material-UI简介
- Tailwind CSS与React
- 组件库选择策略

**学习资源：**
- 📖 [Ant Design React文档](https://ant.design/docs/react/introduce-cn)
- 📖 [Material-UI文档](https://mui.com/zh/material-ui/getting-started/)
- 📖 [Tailwind CSS文档](https://tailwindcss.com/docs/guides/create-react-app)

**练习题：**
1. 使用Ant Design创建管理后台界面
2. 使用Tailwind CSS创建响应式布局
3. 创建自定义主题配置

```jsx
// 练习示例：使用Ant Design
import { Button, Form, Input, Table } from 'antd';

function AdminDashboard() {
  // TODO: 创建管理后台界面
  return (
    <div>
      <Form>
        {/* 表单内容 */}
      </Form>
      <Table 
        columns={columns}
        dataSource={data}
      />
    </div>
  );
}
```

#### Day 46-49: 开发工具与测试
**学习内容：**
- React DevTools使用
- ESLint配置
- 单元测试（Jest + React Testing Library）
- 组件测试策略

**学习资源：**
- 📖 [React Testing Library文档](https://testing-library.com/docs/react-testing-library/intro/)
- 🎥 推荐视频：[React测试教程](https://www.bilibili.com/video/BV1vy4y1C75N)

**练习题：**
1. 为Todo组件编写单元测试
2. 测试自定义Hook
3. 编写集成测试

```jsx
// 练习示例：组件测试
import { render, screen, fireEvent } from '@testing-library/react';

test('计数器增加功能', () => {
  render(<Counter />);
  const button = screen.getByText('增加');
  fireEvent.click(button);
  expect(screen.getByText('1')).toBeInTheDocument();
});
```

### 第8周：综合项目实战

#### Day 50-56: 完整项目开发
**项目选择（选择一个）：**

1. **电商平台前端**
   - 商品列表与详情
   - 购物车功能
   - 用户认证
   - 订单管理
   - 支付流程

2. **社交媒体应用**
   - 用户注册登录
   - 发布动态
   - 点赞评论
   - 关注系统
   - 消息通知

3. **任务管理系统**
   - 项目管理
   - 任务分配
   - 进度跟踪
   - 团队协作
   - 数据统计

**项目要求：**
- 使用React Router实现路由
- 使用Context或Redux管理状态
- 集成UI组件库
- 实现响应式设计
- 包含数据获取和错误处理
- 添加loading和错误提示
- 实现表单验证
- 添加基础测试

**项目结构示例：**
```
src/
├── components/        # 通用组件
│   ├── common/
│   ├── layout/
│   └── ui/
├── pages/            # 页面组件
│   ├── Home/
│   ├── Login/
│   └── Dashboard/
├── hooks/            # 自定义Hooks
├── services/         # API服务
├── store/           # 状态管理
├── utils/           # 工具函数
├── styles/          # 样式文件
└── App.js
```

#### Day 57-60: 项目优化与部署
**学习内容：**
- 性能优化
- SEO优化
- PWA配置
- 部署流程（Vercel/Netlify）

**优化清单：**
- [ ] 代码分割和懒加载
- [ ] 图片优化
- [ ] 缓存策略
- [ ] Bundle分析
- [ ] 错误边界
- [ ] 性能监控

### 📝 第四阶段测验题

1. **项目架构题**
   - 如何组织大型React项目的文件结构？
   - 什么时候应该使用全局状态管理？
   - 如何处理跨组件的业务逻辑？

2. **性能优化题**
   列出你在项目中使用的性能优化技术，并说明原因。

3. **最终项目评估**
   完成的项目应包含：
   - 完整的功能实现
   - 良好的用户体验
   - 代码组织清晰
   - 适当的注释
   - 基础的错误处理

---

## 🎓 学习资源汇总

### 官方文档
- [React官方文档（中文）](https://zh-hans.react.dev/)
- [React Router文档](https://reactrouter.com/)
- [Create React App文档](https://create-react-app.dev/)

### 视频教程推荐
1. **入门级**
   - [React入门到实战（B站）](https://www.bilibili.com/video/BV1wy4y1D7JT)
   - [2024最新React教程（B站）](https://www.bilibili.com/video/BV1Z44y1K7Fj)

2. **进阶级**
   - [React Hooks深度解析](https://www.bilibili.com/video/BV1Ma411h7L6)
   - [React性能优化](https://www.bilibili.com/video/BV1KY4y1M7Ek)

3. **项目实战**
   - [React电商项目实战](https://www.bilibili.com/video/BV1i44y1r7KJ)
   - [React + TypeScript项目](https://www.bilibili.com/video/BV1H44y1j7ww)

### 在线练习平台
- [React Tutorial](https://react.dev/learn/tutorial-tic-tac-toe)
- [CodeSandbox](https://codesandbox.io/)
- [StackBlitz](https://stackblitz.com/)

### 社区资源
- [React中文社区](https://react.docschina.org/)
- [掘金React专栏](https://juejin.cn/tag/React)
- [SegmentFault React标签](https://segmentfault.com/t/react.js)

### 推荐书籍
1. 《React进阶之路》
2. 《深入React技术栈》
3. 《React状态管理与同构实战》

---

## 📊 学习进度追踪表

### 每周学习检查清单

#### 第1周 □
- [ ] 完成开发环境搭建
- [ ] 理解JSX语法
- [ ] 创建第一个组件
- [ ] 完成练习题
- [ ] 通过测验

#### 第2周 □
- [ ] 掌握useState
- [ ] 理解useEffect
- [ ] 组件通信练习
- [ ] 完成练习题
- [ ] 通过测验

#### 第3周 □
- [ ] 创建自定义Hook
- [ ] 性能优化实践
- [ ] 完成练习题
- [ ] 通过测验

#### 第4周 □
- [ ] 表单处理
- [ ] 状态管理进阶
- [ ] 完成练习题
- [ ] 通过测验

#### 第5周 □
- [ ] React Router配置
- [ ] 路由守卫实现
- [ ] 完成练习题
- [ ] 通过测验

#### 第6周 □
- [ ] 数据获取实践
- [ ] 使用React Query
- [ ] 完成练习题
- [ ] 通过测验

#### 第7周 □
- [ ] UI库集成
- [ ] 测试编写
- [ ] 完成练习题
- [ ] 通过测验

#### 第8周 □
- [ ] 完成项目开发
- [ ] 项目优化
- [ ] 项目部署
- [ ] 最终评估

---

## 💡 学习建议

### 对Vue开发者的特别提示

1. **思维转变**
   - Vue的响应式是自动的，React需要手动调用setState
   - Vue有指令系统，React使用JSX表达式
   - Vue的组件是对象配置，React推荐函数组件

2. **相似概念对应**
   - Vue的`data` → React的`useState`
   - Vue的`computed` → React的`useMemo`
   - Vue的`watch` → React的`useEffect`
   - Vue的`methods` → React的普通函数
   - Vue的`v-if` → React的条件表达式
   - Vue的`v-for` → React的`map()`
   - Vue的`slot` → React的`children`
   - Vue的`provide/inject` → React的`Context`

3. **学习重点**
   - 重点理解React的单向数据流
   - 深入学习Hooks的使用和原理
   - 掌握JSX的灵活运用
   - 理解React的渲染机制

### 每日学习流程建议

1. **前10分钟：回顾**
   - 回顾昨天学习的内容
   - 查看笔记和代码

2. **中间40分钟：新知识**
   - 阅读文档
   - 观看视频（1.5-2倍速）
   - 动手编码实践

3. **后10分钟：总结**
   - 整理笔记
   - 记录问题
   - 规划明天

### 常见问题解决

1. **环境问题**
   - 确保Node.js版本 >= 14.0.0
   - 使用npm或yarn，不要混用
   - 遇到依赖问题时删除node_modules重新安装

2. **学习困难**
   - 不要跳跃学习，按顺序进行
   - 每个概念都要动手实践
   - 利用调试工具理解运行机制

3. **项目实践**
   - 从简单项目开始
   - 逐步增加复杂度
   - 参考优秀开源项目

---

## 🎯 学习成果评估标准

### 初级（第1-2周后）
- ✅ 能够创建React应用
- ✅ 理解组件和Props
- ✅ 掌握基础Hook使用
- ✅ 能够处理事件和表单

### 中级（第3-4周后）
- ✅ 能够创建自定义Hook
- ✅ 理解性能优化原理
- ✅ 掌握复杂状态管理
- ✅ 能够处理副作用

### 高级（第5-6周后）
- ✅ 掌握路由配置
- ✅ 能够处理异步数据
- ✅ 理解数据流管理
- ✅ 掌握错误处理

### 实战（第7-8周后）
- ✅ 能够独立完成项目
- ✅ 掌握项目架构设计
- ✅ 理解最佳实践
- ✅ 能够进行性能优化

---

## 🚀 下一步学习方向

完成8周学习计划后，可以继续深入以下方向：

1. **TypeScript + React**
   - 类型安全的React开发
   - 提高代码质量

2. **Next.js**
   - 服务端渲染(SSR)
   - 静态生成(SSG)
   - 全栈开发

3. **React Native**
   - 移动端开发
   - 跨平台应用

4. **高级状态管理**
   - Redux深入
   - MobX
   - Recoil

5. **微前端**
   - Module Federation
   - qiankun

---

## 📝 结语

恭喜你制定了React学习计划！记住，编程学习是一个持续的过程，保持耐心和坚持最重要。遇到困难时不要放弃，多动手实践，多查阅文档，多与社区交流。

**学习编程就像学习一门新语言，需要不断练习才能熟练掌握。加油！💪**

---

*最后更新时间：2024年*
*适用版本：React 18.x*