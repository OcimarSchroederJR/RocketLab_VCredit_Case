# # 🚀 Case V-Credit: Transformação Digital e Inteligência de Dados

> **Contexto:** Rocket Lab 2025 | Visagio
> **Status:** Em desenvolvimento

---

## 📋 Sobre o Projeto
A **V-Credit**, instituição financeira com 30 anos de mercado, enfrenta desafios relacionados à digitalização de seus canais de atendimento. [cite_start]O aumento no volume de interações digitais gerou sobrecarga operacional, custos elevados e dispersão de dados, dificultando a visão estratégica da operação[cite: 11, 16, 22].

Este projeto tem como objetivo estruturar a fundação de dados da V-Credit, implementando uma **Arquitetura Medalhão** robusta no Databricks para garantir integridade, rastreabilidade e escalabilidade das informações. [cite_start]O resultado final visa apoiar a tomada de decisão para redução de custos e melhoria na experiência do cliente[cite: 25, 170].

---

## 🏗️ Arquitetura da Solução
A solução foi desenhada seguindo as melhores práticas de Engenharia de Dados, dividida em camadas lógicas de processamento:

### 🥉 Camada Bronze (Ingestão)
**Objetivo:** Ingestão dos dados brutos ("as-is") provenientes das planilhas fornecidas (Chamados, Clientes, Custos, etc.)[cite: 205].
**Processo:** Carregamento via Databricks Volumes com adição de metadados de controle (`ingestion_timestamp`)[cite: 244].

### 🥈 Camada Silver (Saneamento e Padronização)
* [cite_start]**Objetivo:** Limpeza, tipagem e enriquecimento dos dados[cite: 206].
* **Transformações:**
    * [cite_start]Tratamento de dados nulos e inconsistentes (ex: datas e horas)[cite: 332].
    * [cite_start]Padronização de categorização de motivos (Financeiro, Cartão, etc.)[cite: 153].
    * [cite_start]Criação de chaves para integridade referencial[cite: 415].

### 🥇 Camada Gold (Inteligência de Negócio)
* [cite_start]**Objetivo:** Criação de tabelas Fato e Dimensão otimizadas para análise (BI)[cite: 441].
* [cite_start]**Entregáveis:** Painéis analíticos focados nos KPIs de atendimento, funil de conversão e eficiência operacional[cite: 172].

---

## 🛠️ Tech Stack
* [cite_start]**Plataforma:** Databricks (Community/Free Edition) [cite: 171]
* **Linguagem:** Python (PySpark) & SQL
* [cite_start]**Orquestração:** Databricks Workflows (Jobs Automatizados) [cite: 173]
* **Versionamento:** Git/GitHub

---

## 📂 Estrutura do Repositório
```text
.
├── docs/               # Documentação de negócio, dicionário de dados e imagens
├── notebooks/          # Códigos fonte do ETL
│   ├── 1_bronze/       # Scripts de ingestão
│   ├── 2_silver/       # Scripts de transformação e limpeza
│   └── 3_gold/         # Scripts de agregação e modelagem dimensional
├── dashboard/          # Exportações dos dados para visualização
└── README.md           # Documentação do projeto
