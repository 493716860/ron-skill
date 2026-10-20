# ron-skill — 独立 Skill 仓库

本仓库用于集中管理多个可独立下载、部署的 Skill。**每个 Skill 独立存放在 `skills/<skill-name>/` 下**，内部包含自己的 `SKILL.md`、规则、模板和示例，不依赖其他 Skill。

## 已发布 Skill

| Skill | 版本 | 用途 |
|---|---|---|
| [go-gin-ecommerce](skills/go-gin-ecommerce/) | V3.3 | Go + Gin 电商微信小程序与 Web 运营后台后端研发规范 |
| [wechat-miniprogram](skills/wechat-miniprogram/) | V1.3 | Vue3 + uni-app 微信小程序工程规范（不定义业务需求） |
| [web-admin-frontend](skills/web-admin-frontend/) | V2.0 | Vue3 + Element Plus Web 运营后台工程规范 |
| [product-prototyping](skills/product-prototyping/) | V2.0 | 产品需求规格与 HTML 仿真交互原型设计 |
| [api-database-design](skills/api-database-design/) | V2.0 | OpenAPI 3.1 与 MySQL 8.4 详细设计 |

## 规划中的 Skill（尚未创建）


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

## Skill 职责原则
工程 Skill 约束架构、代码规范、风格和通用技术机制；产品需求设计 Skill 定义业务范围、流程、规则、原型和验收标准。两者不得混淆。
