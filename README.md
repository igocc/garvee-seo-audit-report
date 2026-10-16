# GARVEE SEO 代码规范与四站审计

**[打开单页 HTML](https://igocc.github.io/garvee-seo-audit-report/)**

**[2026-10-16 技术审计 v3：模块 × 页面类型 × 竞品 × 落地](https://igocc.github.io/garvee-seo-audit-report/audit-2026-10-16-module-pagetype.html)**：62 个检查点，按 Meta、URL 与 Sitemap、结构化数据、SSR 主数据区、HTML 语义化、性能六个模块，逐个给出 GARVEE 源码/渲染现状、VEVOR/Amazon/Etsy 实际值、通配符目标规则与示例、Next.js 落地方法和验收标准；含 Claude Opus 5.5 独立复核与实验室测速。

2026-10-15，V5。按“模块 → 页面类型 → 字段取值 → 生成逻辑 → 代码示例 → 实测诊断 → 实施验收”组织。15 个模块、18 个页面与状态族、98 个合同章节、376 行合同表、78 段代码；结构化数据包含 37 组完整模板及明确虚构的 example.invalid 验收夹具。数字描述文档覆盖，不是网站通过率。

快捷入口：[Head](https://igocc.github.io/garvee-seo-audit-report/#module-H) · [HTML 语义与 DOM](https://igocc.github.io/garvee-seo-audit-report/#module-SEM) · [结构化数据](https://igocc.github.io/garvee-seo-audit-report/#module-D) · [SSR](https://igocc.github.io/garvee-seo-audit-report/#module-R) · [robots 联查](https://igocc.github.io/garvee-seo-audit-report/#module-ROB) · [实施工单](https://igocc.github.io/garvee-seo-audit-report/#delivery)

依据飞书同日完整展开快照 revision1156、8 张非空嵌表、相关 SEO Skills 与官方资料；逐模块区分 HTML/Schema 约束、Google 功能资格、可访问性、项目要求及工程建议。示例给出有定义变量、条件、省略/回退和验收，不冒充生产代码或真实商业事实。

项目政策：购物车、登录、注册公共入口允许索引；所有有效关键词且有结果的默认搜索第一页允许索引，无关键词白名单；搜索翻页、排序、组合筛选不索引。普通类目分页独立处理。主数据重要 HTML 必须服务端直接输出，无需页面 JS 才显现。

GARVEE / VEVOR 各 12 个主要样本，Amazon / Etsy 各 2 个选定 SEO 页；另增购物车、默认搜索和 307 响应。28 页正常 DOM 已量测，14 份有效初始页面 HTML（其中 12 份已量测语义）。VEVOR 和 Etsy 未取得的真实初始源码保持未知，不由禁 JS 或正常 DOM 推断完整 SSR 通过。独立 HTTP、禁 JS 和正常 DOM 请求环境分开说明。

本仓库发布单文件报告与说明，不包含飞书全文、认证材料、cookies、原始响应快照、个人会话或评论全文。规范覆盖、实测覆盖、生产实现与实际收录分别标记；本次未修改生产网站。
