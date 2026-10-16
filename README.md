# FORM / 造物 · 3D 打印报价工作台

基于 React 与 Three.js 的桌面浏览器工作台，所有运行依赖嵌入 `index.html`。直接下载 HTML 后用最新版 Edge / Chrome 打开，或通过 GitHub Pages 使用。

## 功能

- STL、OBJ、PLY、3MF、STEP / STP、IGES / IGS、BREP 模型导入与三维预览。
- 每个零件独立设置材料、工艺、后处理、数量及费率；客户和项目资料。
- 体积、重量与报价计算，抽样壁厚分析，可编辑风险规则。
- 导出 Excel、保存 / 恢复项目、报价单预览及浏览器打印为 PDF。

模型在浏览器内处理，不上传至服务器。费率为演示值，请按实际业务修改。壁厚为网格射线抽样估算；未封闭网格不能可靠计算实体体积。SolidWorks / Fusion 原生工程请先导出 STEP。

## 静态发布

在仓库 Settings → Pages 中选择 **Deploy from a branch → main → / (root)**，保存即可。入口为根目录 `index.html`，不需要后端或在线构建。

预期网址：https://sophimotion.github.io/xhijist/

## 开发

可维护的 React / Three.js 源码、测试和构建脚本在 `FORM-source.zip` 中，先解压再运行以下命令。无需重新构建即可直接使用仓库根目录的 `index.html`。

```sh
npm ci
npm test
npm run build
npm run preview
```

构建会更新根目录 `index.html`。依赖目录可在构建后删除，成品无需 Node.js。第三方许可见 `THIRD_PARTY_NOTICES.txt`，也可从应用帮助中导出。
