# 🤖 Chat com PDF usando RAG e Llama 3 (Groq API)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]([analise_documentos_rag_langchain.ipynb](https://github.com/fThauana/chat-pdf-rag/blob/main/analise_documentos_rag_langchain.ipynb))


## 📋 Sobre o Projeto

Este projeto implementa um sistema de **RAG (Retrieval-Augmented Generation)** capaz de ler documentos PDF privados e responder perguntas sobre seu conteúdo utilizando Processamento de Linguagem Natural (NLP).

O objetivo foi criar uma solução de baixo custo computacional e alta performance, substituindo a busca tradicional por palavras-chave por uma **busca semântica** que entende o contexto.

### 🧠 Como funciona?
1. **Ingestão:** O usuário faz upload de um arquivo PDF.
2. **Chunking:** O texto é dividido em pedaços menores para caber na janela de contexto da IA.
3. **Embeddings:** Os textos são convertidos em vetores numéricos usando modelos da HuggingFace.
4. **Vector Search:** Utilizamos o **FAISS** para encontrar os trechos mais relevantes para a pergunta do usuário.
5. **Geração:** O modelo **Llama 3 (via Groq)** gera a resposta final baseada apenas no conteúdo encontrado, reduzindo alucinações.

---

## 🛠️ Tech Stack (Tecnologias)

* **Linguagem:** Python
* **Orquestração:** [LangChain](https://www.langchain.com/)
* **LLM (Cérebro):** Llama 3.3 (via [Groq Cloud](https://groq.com/))
* **Banco Vetorial:** FAISS (Facebook AI Similarity Search)
* **Embeddings:** Sentence-Transformers (HuggingFace)
* **Ambiente:** Google Colab

---

## 🚀 Como executar este projeto

A maneira mais fácil de testar é utilizando o **Google Colab**, pois o ambiente já está configurado.

1.  **Clique no botão "Open in Colab"** no topo deste README.
2.  Gere uma API Key gratuita na [Groq Cloud](https://console.groq.com/keys).
3.  No menu lateral esquerdo do Colab, faça upload de um arquivo PDF e renomeie para `documento.pdf`.
4.  Execute as células sequencialmente.
5.  Quando solicitado, insira sua chave de API (o input é protegido/invisível por segurança).

---

## 📂 Estrutura do Notebook

O código foi modularizado em etapas claras:
* **Instalação de Dependências:** Versões travadas para garantir estabilidade (`langchain==0.1.20`, `numpy<2`).
* **Configuração de Ambiente:** Validação de API Keys e arquivos.
* **Pipeline de ETL:** Carregamento e Fatiamento (Splitting) do PDF.
* **Indexação:** Criação da memória vetorial.
* **Interface de Chat:** Loop interativo para conversar com o documento.

---

## ⚠️ Dependências (requirements.txt)

Caso queira rodar localmente, estas são as bibliotecas principais:

```txt
langchain==0.1.20
langchain-community==0.0.38
langchain-groq
faiss-cpu
pypdf
sentence-transformers
numpy<2
```

---

## 👤 Autor
Desenvolvido por **Thauana Farias** durante estudos de NLP e IA Generativa.

Entre em contato! 

 <a href="https://www.linkedin.com/in/thauana-vitoria-ferreira-farias" target="_blank">
    <img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank">
  </a>
