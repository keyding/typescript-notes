# `TypeScript` 定义

## TypeScript 是什么?

- JavaScript 的一个超集
- 强类型，支持静态和动态类型
- 在编译阶段检查类型错误
- 本质上向 `JavaScript` 添加了可选的静态类型和基于类的面向对象编程
- 最终编译为 `JavaScript`

## 使用 `TypeScript`

### 本地安装

1.安装 `TypeScript`

```bash
$ yarn global add typescript (npm install -g typescript)
```

2.查看版本号

```
$ tsc -v
Version 4.0.2
```

3.编译 `TypeScript` 文件 

```
$ tsc test.ts # 生成 test.js 文件
```

### `TypeScript` Playground

不需要本地安装 `typescript`, 线上直接可用。可通过配置 `TS Config` 的 `Target`，可以设置不同的编译目标，从而编译生成不同的目标代码。

[TypeScript Playgrond](https://www.typescriptlang.org/play)

## TypeScript 初体验

新建 `.ts` 文件 [test.ts](example/1_what_is_typescript/test.ts)，并输入如下代码

```typescript
function getAppName(app: string): string {
    return `${app}: appname`;
}

console.log(getAppName('typescript'));
```

编译 `test.ts` 文件

```bash
$ tsc test.ts
```

生成 `test.js`

```javascript
function getAppName(app) {
    return app + ": xxxxx";
}
console.log(getAppName('typescript'));
```

生成的 [`test.js`](example/1_what_is_typescript/test.js) 文件的类型被擦除，TypeScript 只会在编译阶段对类型进行静态检查，发现错误，及时报错。编译后就是普通的 `JavaScript` 代码。