## 目录

1. 泛型的作用

    [泛型](https://www.tslang.cn/docs/handbook/generics.html)

2. unknown 类型

    > unknown 类型不能赋值给除了 unknown 或 any 的其他任何类型，使用前必需显式进行指定类型，或是在有条件判断情况下能够隐式地进行类型推断的情况

    unknown 和 any 的主要区别

    * 新的 unknown 类型，它是 any 类型对应的安全类型。

    * unknown 类型会更加严格：在对 unknown 类型的值执行大多数操作之前，我们必须进行某种形式的检查。
    
    * 在对 any 类型的值执行操作之前，我们不必进行任何检查

3. interface 和 type 到底有什么区别

    [参考文档](https://www.typescriptlang.org/docs/handbook/advanced-types.html#type-aliases)

    - 相同点

        - 都可以描述一个对象或者函数
        - 都允许拓展（interface extends）但语法不同，type 是通过联合来实现扩展
        - type 类型别名能被 extends 和 implements

        ```ts
        // extends
        type Parent = { x: number }
        interface Child extends Parent {
            y: number
        }

        // implements
        type Point2 = {
            x: number
            y: number
        }
        class SomePoint2 implements Point2 {
            x = 1
        }
        ```

    - 不同点
        - type 可以声明基本类型别名，联合类型，元组等类型，interface 不可以
        - type 还可以使用 typeof 获取实例的 类型进行赋值
        - interface 能够声明合并，type 不可以
        - type 类型别名不能被 extends 和 implements

4. 高级类型

    https://www.tslang.cn/docs/handbook/advanced-types.html

5. TypeScript 的高级类型
   https://juejin.im/post/5eb6d9cde51d454de777297d?utm_source=gold_browser_extension

## 参考资料

* [如何编写一个 d.ts 文件](https://segmentfault.com/a/1190000009247663)
