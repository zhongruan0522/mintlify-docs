# AGENTS.md

本仓库是 NookMux 产品文档与个人技术文档共用的 Mintlify 站点。修改本仓库前先读这里。

## 站点结构

- `docs.json` 是站点唯一配置：导航、语言、主题全部在此定义。**新增/改名/删除页面必须同步更新 `docs.json`**，否则页面不出现在侧栏。
- 站点采用 Mintlify i18n 语言结构（`navigation.languages`）：
  - `cn`（默认语言）：个人内容（`vibe-coding/`、`antihub-all/`，页面在站点根）+ NookMux 中文文档（`cn/nookmux/`）
  - `en`：NookMux 英文文档（`nookmux/`）
- 页面路径规则：默认语言 cn 的个人内容与 NookMux 英文页面不强制语言前缀（NookMux 内容统一带 `nookmux/` 前缀），cn 语言的 NookMux 页面路径以 `cn/nookmux/` 开头。
- 内部链接：cn 页面用 `/cn/nookmux/...`，en 页面用 `/nookmux/...`；个人中文内容页面用根相对路径（`/vibe-coding/...`）。
- API 端点页（`nookmux/api/`、`cn/nookmux/api/`）使用 frontmatter `api: "METHOD /path"` 声明端点，正文只保留描述；`{model}` 路径参数与 Gemini `:action` 后缀是合法写法。

## 约定

- NookMux 文档区（`nookmux/`、`cn/nookmux/`）两语言文件一一对应，改一侧内容时同步另一侧。
- 组件全部使用 Mintlify 内置组件（`Note`/`Warning`/`Info`、`Card`+`Columns`、`Tabs` 等），无需 import；带标题的提示用 `<Card type="info|warning" title="...">`。
- 不要在页面里手写相对路径链接，统一根相对路径。

## 验证

推送前在仓库根执行：

```bash
mint validate
mint broken-links
```

两者必须全绿（已知豁免：`assets/nookmux/langbot/` 图片尚未补入前的 14 处图片断链）。
