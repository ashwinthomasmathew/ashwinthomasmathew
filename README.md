# Ashwin Thomas Mathew

Data engineer working on data platforms and applied AI. I'm currently Assistant Manager, Data & AI at [R for Rabbit](https://www.rforrabbit.com), where I build the company's data platform and the AI tools that run on top of it. Before that I spent three years as a Business Intelligence Engineer at Amazon.

Most of what I build at work lives in private repositories, so this page describes it instead of linking to it.

Based in Ahmedabad, open to relocating. I grew up in the UAE.

## Current work

### D2C data platform on Azure

Ingestion and processing for Shopify, Unicommerce and ClickPost, orchestrated by Azure Data Factory with Python runbooks, ADLS Gen2 storage and Synapse serverless SQL. It runs three times a day and covers 109K+ orders and ₹25 Cr+ in sales. Each load is written as an immutable Parquet release that has to pass reconciliation and validation gates before it is promoted, so any release can be rolled back without losing data. In October 2026 I audited it field by field against the vendors' own exports and repaired the defects that turned up, including tracking numbers that Excel had turned into scientific notation before upload.

### R4R D2C Data, an MCP connector for Claude

A remote MCP server on Azure Container Apps that lets people at R for Rabbit ask Claude about live order, shipment and product data from claude.ai. Sign-in goes through Microsoft Entra (OAuth with PKCE), every query is read-only SQL checked against guard rails, and the database role can only see a curated `agent` schema. Before writing SQL the model reads a business-context file of join keys, default scopes and interpretation rules. When an answer or a dashboard built on the connector gets the business wrong, the fix usually goes into that file, after checking the claim against source data.

### Other MCP servers

- A read-only Keka HR connector for Claude Desktop. Personal fields such as addresses, bank details and PAN are dropped in code before anything reaches the model.
- A read-only Shopify analytics MCP for Genspark on Azure Container Apps, since retired.

### Reporting and automation

- A Power BI leadership dashboard for delivery TAT against a two-day target, warehouse allocation, SDD/NDD and courier NDR/RTO.
- Earlier versions of the platform on Microsoft Fabric (Bronze, Silver and Gold layers with a Direct Lake model), plus a Databricks Genie proof of concept for natural-language questions.
- Power Automate and Office Scripts flows that log about 800 material-receipt emails a month into a validated Excel register, and a Google Sheets to Excel sync for quick-commerce PO tracking that saves about 34 hours a week.
- A React and TypeScript app that hosts single-file HTML dashboards behind Entra sign-in, with SharePoint as the storage layer.

## Before R for Rabbit

At Amazon (2022 to 2025) I built AWS ETL and inference services on Lambda, S3, Redshift and Python that supported more than a million price points a day, and worked on a Bedrock-based RAG setup for Redshift query optimisation with guardrails against prompt injection and data leakage. I also mentored over 200 analysts and received six Stellar Awards. After Amazon I ran category and data operations at FYVA across 50+ brands.

I studied mechanical engineering at Saintgits College of Engineering, where I was chassis head of Madbolt Formula Racing for Formula Bharat 2021.

## Tools

![Python](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05033?style=flat-square&logo=git&logoColor=white)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=claude&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square&logo=modelcontextprotocol&logoColor=white)

Certifications: AWS Certified Solutions Architect - Associate, Claude Code in Action (Anthropic), Developing Applications with Apache Spark (Databricks).

## Elsewhere

- Writing: [substack.com/@techiejots](https://substack.com/@techiejots) and [Medium](https://medium.com/@ashwinthomasmathew99)
- Practice: [neetcode-submissions](https://github.com/ashwinthomasmathew/neetcode-submissions)
- [LinkedIn](https://www.linkedin.com/in/ashwinthomasm/) | [Stack Overflow](https://stackoverflow.com/users/30773642) | [ashwinthomasmathew99@gmail.com](mailto:ashwinthomasmathew99@gmail.com)
