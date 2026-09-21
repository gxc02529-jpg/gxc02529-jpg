<div align="center">

# 企业级 RAG / Agent 参考实现

统一交付底座 · 三个脱敏业务场景

围绕一套统一的 RAG / Agent 交付底座，为物流售后、SaaS 技术支持、招聘协作三类场景提供脱敏参考实现。

![Python](https://img.shields.io/badge/Python-3.11%20%7C%203.12%20%7C%203.13-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square)
![Milvus](https://img.shields.io/badge/Milvus-00A1EA?style=flat-square)
![MCP](https://img.shields.io/badge/MCP-FastMCP-6E4AFF?style=flat-square)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

</div>

---

## 仓库

| 仓库 | 业务场景 | 关键实现 | CI |
| --- | --- | --- | --- |
| **[KnowLoop](https://github.com/gxc02529-jpg/KnowLoop)** | 物流售后知识问答 | FAQ 高置信直出；Dense + BM25 混合检索、重排与引用生成；多租户范围与知识版本（staged / active / archived）治理；离线检索评测与反馈收集 | [![CI](https://github.com/gxc02529-jpg/KnowLoop/actions/workflows/ci.yml/badge.svg)](https://github.com/gxc02529-jpg/KnowLoop/actions) |
| **[CaseOps](https://github.com/gxc02529-jpg/GA)** | SaaS 技术支持工单 | 工单接入 → 同源聚合 → 信息补齐 → 证据检索 → 人工审批 → 独立处置 → 知识回流；LangGraph 条件路由（CLARIFY / SINGLE / PIPELINE）；混合检索与引用白名单校验 | [![CI](https://github.com/gxc02529-jpg/GA/actions/workflows/ci.yml/badge.svg)](https://github.com/gxc02529-jpg/GA/actions) |
| **[HireAgent](https://github.com/gxc02529-jpg/HireAgent)** | 招聘协作 Agent | 13 个可调用工具 / 3 个职责受限 Agent / 9 类结构化意图；FastMCP 提供 STDIO 与 Streamable HTTP 两种传输；规则化可解释评分，评分不使用年龄、性别等个人属性 | [![CI](https://github.com/gxc02529-jpg/HireAgent/actions/workflows/ci.yml/badge.svg)](https://github.com/gxc02529-jpg/HireAgent/actions) |

三个仓库共用同一套交付底座，按场景做配置化适配；业务资料彼此隔离，同一底座可跨行业复用。

---

## 工程关注点

**可验证性**

- 多 Python 版本矩阵（3.11 / 3.12 / 3.13），每次推送执行字节编译与回归测试。
- 不依赖模型与外部数据库的检查单独拆出，保证 CI 无需 GPU 与向量库即可跑通。

**依赖安全**

- 以 [OSV](https://osv.dev) 扫描固定依赖的已知漏洞，按包聚合，给出可一次清空该包全部告警的目标版本。
- 依赖解析（`pip install --dry-run`）、按声明版本安装、运行时导入冒烟三步接入 CI：能解析不代表能导入，跨版本升级的问题集中在后者。
- 漏洞扫描当前以报告形式接入（只提示不阻断），基线清零后再设为硬卡口。

**边界标注**

- 每个仓库明确区分已实现能力与尚未接线的部分（模型服务、生产数据库、外部业务系统），不将示例视为生产实现。
- 仓库内业务数据均为自建合成样例，不代表任何真实机构政策。

---

<div align="center">

<sub>仓库内容用于技术验证与交付底座复用演示，不作为生产系统直接部署使用。</sub>

</div>
