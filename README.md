# mintlify-docs

个人 Mintlify 文档站，托管两类内容：

- **AI 编码教程**（`vibe-coding/`）与 antihub 部署文档（`antihub-all/`）——中文
- **NookMux 产品文档**（`nookmux/` 英文、`cn/nookmux/` 中文）——从 NookMux 主仓库迁移的双语文档站

## 开发

```bash
npm i -g mint
mint dev        # 本地预览 http://localhost:3000
```

## 推送前校验

```bash
mint validate
mint broken-links
```

站点配置集中在 `docs.json`（语言结构、导航、主题）；新增页面必须同步更新导航，否则不会出现在侧栏。
