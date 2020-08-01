# TS

## Q: TS 的优势是什么？用 TS 有什么好处？

### 特点：

1. 静态代码解析
2. 代码有错误仍然可以生成 js 文件，但不一定可以执行

### 基础类型：

关键字 变量：类型 = 初始值

1. string
2. number
3. boolean
4. 数组
   1. 类型[]
   2. 泛型： Array<类型>
5. 元组：已知元素的类型和位置的数组，如果访问越界元素（超过已有下标），则所有已有类型都可以使用
6. 枚举 enum 可以通过值找到键
7. any 未知类型，可能来自用户输入或者第三方库
8. void 函数没有返回值时表示
9. null 和 undefined 默认为所有类型的子类型，但是推荐使用严格类型检查--strictNullChecks
10. never 类型： 抛出异常或者不会有返回值的函数，当表示变量类型时则变量永不为真
11. Object 引用类型
12. 类型断言
    1. <>语法
    2. as 语法
13. 接口 interface
    1. 语法： `interface 类型名称 {属性名: 属性类型;}`
    2. 可选属性： 属性后面加？
    3. 只读属性： 属性前面加 readonly 【注：变量用 const,属性用 readonly】
    4. 任意类型的其他属性 `[propName: string]：any`
    5. interface 表示函数 `interface FuncType {(source: string, substring: string): boolean;}` 调用时名称不一定一致，但是顺序一致

### 泛型

类型变量 T: 用于表示类型而不是值，可用于捕获类型（ts 中能当类型入口的只有泛型）

### 避过类型检查

1. 赋值

### 类型守卫

作用: 缩小类型范围

1. instanceof
2. in
3. 字面量

### class

利用 class 统一管理类型和初始化默认值

### typescript 与 react

1. @type 表示引用 js 库的 ts 声明文件
2. 无状态组件 type SFC<P> React.SFC<IProps>
3. 有状态组件 Component<P, S>

### 类型工具

1. Partial
   1. 只能让外层属性变成可选，不能让深层属性变成可选
