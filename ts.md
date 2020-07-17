# TS
### 特点：
1. 静态代码解析
2. 代码有错误仍然可以生成js文件，但不一定可以执行

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
9. null和undefined默认为所有类型的子类型，但是推荐使用严格类型检查--strictNullChecks
10. never类型： 抛出异常或者不会有返回值的函数，当表示变量类型时则变量永不为真
11. Object 引用类型
12. 类型断言
    1.  <>语法
    2.  as语法
13. 接口interface
    1.   语法： ``interface 类型名称 {属性名: 属性类型;}``
    2.   可选属性： 属性后面加？
    3.   只读属性： 属性前面加 readonly  【注：变量用const,属性用readonly】
    4.   任意类型的其他属性 ``[propName: string]：any``
    5.   interface表示函数 ``interface FuncType {(source: string, substring: string): boolean;}`` 调用时名称不一定一致，但是顺序一致

### 泛型
   类型变量T: 用于表示类型而不是值，可用于捕获类型


### 避过类型检查
1. 赋值