# MySQL 数据库规范
表和每个字段都必须包含有意义的中文 COMMENT，新增/修改字段均遵守。使用 InnoDB、utf8mb4。主键统一 BIGINT UNSIGNED（生成策略由项目统一决定），金额 BIGINT 表示分，数量整数，时间 DATETIME(3) 并明确时区约定。必须按业务设计 NOT NULL、默认值、唯一键和必要索引；敏感字段最小化存储。Schema 变更使用版本化 SQL Migration；禁止直接在生产环境手工改表。禁止使用浮点金额。示例：`price_amount BIGINT NOT NULL COMMENT '商品售价，单位：分'`。
