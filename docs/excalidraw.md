# 编辑博客图表

在 VS Code 安装 Excalidraw 扩展（`pomdtr.excalidraw-editor`）。仓库已配置扩展推荐。

打开 `source/images/agent-products.excalidraw.svg` 即可用图形编辑器修改“产品形态”。该文件同时包含 SVG 图片和可编辑的 Excalidraw 场景，文字、方框和分隔线均可单独编辑。保存后运行 `npm run build`，或在 `npm run server` 本地预览中刷新页面。

新增图表时，在 `source/images/` 创建空的 `名称.excalidraw.svg`，使用扩展绘图并保存。在文章中引用：

```markdown
![图表说明](/images/名称.excalidraw.svg)
```

使用 Excalidraw 网页版导出 SVG 时，勾选嵌入场景（Embed scene），以便后续继续编辑。

网页通过普通图片展示 SVG，无需加载 Excalidraw JavaScript，也不提供在线编辑画布。重新构建和部署后，线上图表才会更新。

注意：直接编辑 SVG 的可见 XML 不会同步嵌入场景，请使用 Excalidraw 图形编辑器修改和保存。

官方扩展说明：https://github.com/excalidraw/excalidraw-vscode#edit-images
