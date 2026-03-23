# LVGL Pro UI Simulator Starter

这个仓库是一个适合 `LVGL Pro` 打开、继续设计、导出和在 CI 中处理的最小项目骨架。

## 为什么这个结构是“符合条件”的

根据 LVGL Pro 官方文档，一个可被识别为 **Project** 的代码库，至少需要：

- 根目录存在 `project.xml`
- 根目录存在 `globals.xml`
- 用目录组织 `screens`、`components`、`widgets`、`fonts`、`images`

其中：

- `project.xml` 用来把整个项目组织起来，也可以引用外部组件库
- `globals.xml` 用来存放全局样式、主题常量、subjects 等
- `screens/*.xml` 放页面
- `components/*.xml` 放可复用组件
- `widgets/*.xml` 放自定义 widget

## 当前内容

- `project.xml`: 项目标识和外部组件库入口
- `globals.xml`: 一个最小的全局样式和 subject 示例
- `screens/home.xml`: 一个可继续扩展的示例首页

## 推荐工作流

1. 用 LVGL Pro 打开这个仓库根目录
2. 在 `screens/` 下继续新建页面
3. 在 `components/` 下拆分复用组件
4. 需要校验或导出时，使用 LVGL Pro CLI 处理整个项目目录

官方文档提到的常见命令包括：

```bash
lved-cli.js validate .
lved-cli.js generate .
lved-cli.js compile . --target web --start-service
```

说明：

- `validate` 用来检查 XML
- `generate` 用来导出 C/H
- `compile --target web` 可用于预览/测试工作流

## 后续你可以怎么扩展

- 把 `home.xml` 拆成多个 screen
- 新增 `components/top_bar.xml`、`components/status_card.xml`
- 在 `project.xml` 里加入共享组件库
- 在 `tests/` 下加入 UI 测试 XML

## 参考

- LVGL Pro Files: https://docs.pro.lvgl.io/files.html
- LVGL Pro Project Setup: https://docs.pro.lvgl.io/project_setup.html
- LVGL Pro Creating Screens: https://docs.pro.lvgl.io/screens.html
- LVGL Pro CLI: https://docs.pro.lvgl.io/tools/cli.html
