# ron-skill — 独立 Skill 仓库

本仓库用于集中管理多个可独立下载、部署的 Skill。**每个 Skill 独立存放在 `skills/<skill-name>/` 下**，内部包含自己的 `SKILL.md`、规则、模板和示例，不依赖其他 Skill。

## 已发布 Skill

| Skill | 版本 | 用途 |
|---|---|---|
| [go-gin-ecommerce](skills/go-gin-ecommerce/) | V3.2 | Go + Gin 电商微信小程序与 Web 运营后台后端研发规范 |

## 规划中的 Skill（尚未创建）

- `skills/product-prototyping/`：产品需求、业务规则、交互原型设计
- `skills/wechat-miniprogram/`：微信小程序前端开发
- `skills/web-admin-frontend/`：Web 运营后台前端开发

## 单独下载与部署

**推荐：Git sparse-checkout**（只拉取一个 Skill）：

```bash
git clone --filter=blob:none --no-checkout https://github.com/493716860/ron-skill.git
cd ron-skill
git sparse-checkout init --cone
git sparse-checkout set skills/go-gin-ecommerce
git checkout main
```

目标项目中仅复制 `skills/go-gin-ecommerce/` 下的内容到该项目的 AI Skill 目录；根据所用 AI 工具要求配置入口。各 Skill 以自身 `SKILL.md` 为主入口。复制到项目根目录使用时，应避免覆盖项目已有的 `AGENTS.md`。

新增 Skill 时，在 `skills/` 下新建独立子目录，不要在仓库根目录直接放业务专项规范。
