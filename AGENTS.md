# AGENTS.md

个人 Mintlify 文档站（mintlify-docs），内容定位与目录说明见 README.md。当前主要托管
NookMux 产品文档（英文 `nookmux/`、中文 `cn/nookmux/`），公共片段在 `snippets/`。

## 命令

- 安装工具：`npm i -g mint`
- 本地预览：`mint dev`（http://localhost:3000）
- 推送前校验：`mint validate` 与 `mint broken-links`

## 关键约定

- 站点配置集中在 `docs.json`（语言结构、导航、主题）；新增页面必须同步更新
  `docs.json` 导航，否则不会出现在侧栏。
- `nookmux/`（英文）与 `cn/nookmux/`（中文）是同一套文档的两种语言，改动一侧
  必须检查另一侧是否需要同步。
- 本站只放面向用户的产品文档；NookMux 主仓库的内部开发文档不要混入。
