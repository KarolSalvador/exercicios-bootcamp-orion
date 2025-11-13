# 🚀 Classificador de Intenção com Múltiplos Agentes (Flowise + Qdrant + Gemini)

Esta atividade, realizada para o Bootcamp ORION, demonstra a criação de um fluxo de trabalho de Inteligência Artificial Conversacional que utiliza um Classificador de Intenção para rotear perguntas a Agentes Especialistas conectados a bases de conhecimento (RAG).

---

## 🎥 Demonstração em Vídeo

Assista a uma demonstração rápida do fluxo e do roteamento automático para os agentes:

[Demo Agentflow funcionando](https://youtu.be/URd0UE0-8DY)

---

## 🎯 Objetivo

Criar um sistema capaz de:

1.  Classificar a intenção do usuário em uma de três categorias: **Economia**, **Saúde** ou **Tecnologia**.
2.  Roteá-la automaticamente para o Agente especialista correto.
3.  Utilizar Document Stores separados (Qdrant) para garantir que cada Agente responda apenas com base em informações relevantes do seu escopo.

---

## 🛠️ Tecnologias Utilizadas

<div align=center>

![Flowise Badge](https://img.shields.io/badge/Flowise-000000?style=for-the-badge&logo=flowise&logoColor=white)
![Qdrant Badge](https://img.shields.io/badge/Qdrant-000000?style=for-the-badge&logo=qdrant&logoColor=white)
![Google Gemini](https://img.shields.io/badge/google%20gemini-8E75B2?style=for-the-badge&logo=google%20gemini&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Docker Compose](https://img.shields.io/badge/Docker--Compose-D9E7FF?style=for-the-badge&logo=docker&logoColor=2496ED)

</div>

- **Orquestração/Flow:** Flowise
- **Vector Database (Document Store):** Qdrant
- **Modelo de Linguagem (LLM):** Gemini (Google AI Studio)
- **Containerização:** Docker e Docker Compose

---

## 📂 Estrutura de Entrega

| Arquivo/Pasta            | Conteúdo                                                              |
| :----------------------- | :-------------------------------------------------------------------- |
| `fluxo_condicional.json` | Exportação do fluxo completo do Flowise.                              |
| `_prints/`               | Imagens dos três Document Stores criados.                             |
| `_docs_entrega/`         | Documentos de texto originais utilizados para popular as bases.       |
| `docker-compose.yml`     | Arquivo de orquestração do ambiente, que inicia o Flowise e o Qdrant. |
| `README.md`              | Este documento de explicação.                                         |

---

## ⚙️ Como Executar Localmente

Para rodar este projeto, você precisará de **Docker** instalado e das chaves de API.

1.  **Configurar Variáveis:** Crie um arquivo `.env` na raiz do projeto (fora do escopo deste repositório público) com as suas chaves:

    ```
    GEMINI_API_KEY=sua_chave_do_gemini
    QDRANT_API_KEY=sua_chave_do_qdrant
    ```

2.  **Docker Compose:** Utilize o `docker-compose.yml` e execute:

    ```bash
    docker compose up -d
    ```

3.  **Importar Fluxo:** Acesse o Flowise (`localhost:3000`), importe o `fluxo_condicional.json` e configure as credenciais para o Gemini e Qdrant usando as chaves do seu `.env`.

---
