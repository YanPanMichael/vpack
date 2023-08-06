### 安装

```bash
npm i -D @autopack/vpack # 或 yarn add -D @autopack/vpack
```

### 使用

**第一步**：package.json 中新增 scripts：

```js
  "scripts": {
    "build": "NODE_ENV=production vpack build --source=ts"
  },
```

需要通过参数`source`指定构建打包源文件格式，其取值为`'js', 'ts'`格式之一。

**第二步**：命令行进入项目目录，运行：

```bash
npm run build # 或 yarn build
```

@autopack/vpack 默认以 `src/index.ts` 为入口，在 `dist` 目录输出 `'umd', 'es', 'cjs', 'iife', 'amd'` 五种格式的构建包（包含未压缩和已压缩版本）。