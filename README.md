<div align="center">
  <img src="./assets/profile-banner.svg" width="100%" alt="Build systems that ship — Agent Systems, RAG, MCP, A2A and Platform Engineering" />

  <br />

  ![Focus](https://img.shields.io/badge/FOCUS-Production_AI_Systems-0f172a?style=for-the-badge&labelColor=0f172a&color=22d3ee)
  ![Quality](https://img.shields.io/badge/QUALITY-Tested_%C2%B7_Observable_%C2%B7_Maintainable-0f172a?style=for-the-badge&labelColor=0f172a&color=818cf8)
  ![Data](https://img.shields.io/badge/PUBLIC_DATA-Synthetic_%26_Desensitized-0f172a?style=for-the-badge&labelColor=0f172a&color=4ade80)
</div>

## Featured Systems

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/gxc02529-jpg/shopagent-pro">ShopAgent Pro</a></h3>
      <p>全渠道电商多智能体客服中台。商品、推荐、订单与售后领域隔离，生产主链路真实跨越 A2A 与 MCP，包含反馈审核、知识发布和后续复用闭环。</p>
      <p><code>FastAPI</code> <code>Multi-Agent</code> <code>MCP</code> <code>A2A</code> <code>Redis</code> <code>MySQL</code></p>
      <a href="https://github.com/gxc02529-jpg/shopagent-pro/actions/workflows/ci.yml"><img src="https://github.com/gxc02529-jpg/shopagent-pro/actions/workflows/ci.yml/badge.svg" alt="ShopAgent Pro CI" /></a>
      <a href="https://github.com/gxc02529-jpg/shopagent-pro/releases"><img src="https://img.shields.io/github/v/release/gxc02529-jpg/shopagent-pro?style=flat-square&label=release" alt="ShopAgent Pro release" /></a>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/gxc02529-jpg/enterprise-sales-agent">Enterprise Sales Agent</a></h3>
      <p>企业销售分析 Agent。围绕状态编排、工具协议、检索增强与知识关系构建可验证的数据分析链路，公开演示数据已脱敏。</p>
      <p><code>LangGraph</code> <code>FastMCP</code> <code>RAG</code> <code>Knowledge Graph</code></p>
      <a href="https://github.com/gxc02529-jpg/enterprise-sales-agent/actions/workflows/ci.yml"><img src="https://github.com/gxc02529-jpg/enterprise-sales-agent/actions/workflows/ci.yml/badge.svg" alt="Enterprise Sales Agent CI" /></a>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/gxc02529-jpg/CaseOps">CaseOps</a></h3>
      <p>SaaS 技术支持工单编排。通过 LangGraph 条件路由、混合检索、引用白名单、人工审批与知识回流控制自动化边界。</p>
      <p><code>LangGraph</code> <code>Hybrid Retrieval</code> <code>Approval Gates</code> <code>FastAPI</code></p>
      <a href="https://github.com/gxc02529-jpg/CaseOps/actions/workflows/ci.yml"><img src="https://github.com/gxc02529-jpg/CaseOps/actions/workflows/ci.yml/badge.svg" alt="CaseOps CI" /></a>
      <a href="https://github.com/gxc02529-jpg/CaseOps/releases"><img src="https://img.shields.io/github/v/release/gxc02529-jpg/CaseOps?style=flat-square&label=release" alt="CaseOps release" /></a>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/gxc02529-jpg/KnowLoop">KnowLoop</a></h3>
      <p>物流售后知识问答。覆盖 FAQ 直出、Dense + BM25 多路召回、重排与引用，以及租户范围和知识版本治理。</p>
      <p><code>RAG</code> <code>Dense + BM25</code> <code>Reranking</code> <code>Knowledge Governance</code></p>
      <a href="https://github.com/gxc02529-jpg/KnowLoop/actions/workflows/ci.yml"><img src="https://github.com/gxc02529-jpg/KnowLoop/actions/workflows/ci.yml/badge.svg" alt="KnowLoop CI" /></a>
      <a href="https://github.com/gxc02529-jpg/KnowLoop/releases"><img src="https://img.shields.io/github/v/release/gxc02529-jpg/KnowLoop?style=flat-square&label=release" alt="KnowLoop release" /></a>
    </td>
  </tr>
  <tr>
    <td colspan="2" valign="top">
      <h3><a href="https://github.com/gxc02529-jpg/HireAgent">HireAgent</a></h3>
      <p>招聘协作 Agent。13 个工具调用、3 个职责受限 Agent 与 9 类结构化意图，通过 FastMCP 和 FastAPI 提供可解释匹配与幂等排期。</p>
      <p><code>FastMCP</code> <code>Scoped Agents</code> <code>Structured Intent</code> <code>Idempotency</code></p>
      <a href="https://github.com/gxc02529-jpg/HireAgent/actions/workflows/ci.yml"><img src="https://github.com/gxc02529-jpg/HireAgent/actions/workflows/ci.yml/badge.svg" alt="HireAgent CI" /></a>
      <a href="https://github.com/gxc02529-jpg/HireAgent/releases"><img src="https://img.shields.io/github/v/release/gxc02529-jpg/HireAgent?style=flat-square&label=release" alt="HireAgent release" /></a>
    </td>
  </tr>
</table>

## System Design

```text
Client / Channel
       │
       ▼
API Gateway ── Identity · Rate Limit · Trace · Streaming
       │
       ▼
Orchestrator ── Intent · State · Routing · Approval · Fallback
       │
       ├── Domain Agents ── Product · Order · Support · Analytics
       │         │
       │         └── MCP Tools ── Schema · Auth · Timeout · Circuit Breaker
       │
       └── Knowledge ── Hybrid Recall · Rerank · Citation · Versioning
                 │
                 ▼
Data & Operations ── Redis · SQL · Vector Store · Audit · Metrics
```

## Engineering Stack

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=for-the-badge&logo=pydantic&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-111827?style=for-the-badge)
![MCP](https://img.shields.io/badge/MCP-6D5DFB?style=for-the-badge)
![A2A](https://img.shields.io/badge/A2A-0891B2?style=for-the-badge)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Milvus](https://img.shields.io/badge/Milvus-00A1EA?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)

</div>

## Quality Bar

| Runtime | Verification | Safety | Operations |
|---|---|---|---|
| 本地最小路径可运行 | 单元、协议与端到端测试 | 合成/脱敏公开数据 | Health / Ready / Metrics |
| 明确生产传输边界 | 多 Python 版本 CI | 身份、权限与幂等 | Trace、审计与告警接口 |
| 可插拔模型与存储 | 锁定依赖与镜像构建 | PII 处理与审批门禁 | 降级、熔断与恢复路径 |

<div align="center">
  <sub>Design boundaries. Verify behavior. Ship maintainable systems.</sub>
</div>
