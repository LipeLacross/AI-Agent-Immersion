## 🌐 [English Version of README](README_EN.md)

# AI agnet immersion

**Masterclass**  
- https://guilhermeonrails.github.io/materclass-python-ia-agentes/#cap5  
- https://fiapcom.sharepoint.com/sites/Alura/Documents/Forms/AllItems.aspx?id=%2Fsites%2FAlura%2FDocuments%2FAlura%20%5F%20Growth%2F2%2E%20Product%20Marketing%2FCompartilhados%20externos%2FImers%C3%A3o%20Dev%20Agentes%20IA%2FPython%2DMasterclass%201%2Epdf&parent=%2Fsites%2FAlura%2FDocuments%2FAlura%20%5F%20Growth%2F2%2E%20Product%20Marketing%2FCompartilhados%20externos%2FImers%C3%A3o%20Dev%20Agentes%20IA&p=true&ga=1  

**API Key do Google**  
- https://aistudio.google.com/app/apikey  

**Baixar PDFs usados na aula**  
- https://fiapcom.sharepoint.com/sites/Alura/Documents/Forms/AllItems.aspx?id=%2Fsites%2FAlura%2FDocuments%2FAlura%20%5F%20Growth%2F2%2E%20Product%20Marketing%2FCompartilhados%20externos%2FImers%C3%A3o%20Dev%20Agentes%20IA%2FPDFs%20Aula%202&viewid=a4e246d8%2D2213%2D4b9d%2D980e%2D02833d082636&ga=1  

---

# AI-Agent-Immersion

Este repositório contém materiais e notebooks da **Imersão em Agentes de IA**, explorando desde noções básicas de Python até a construção de agentes inteligentes usando **LangChain**, **Google Gemini** e **LangGraph**.

O objetivo é implementar um **agente de Service Desk** capaz de:
- Fazer triagem automática de mensagens (classificação estruturada).
- Responder perguntas com **RAG (Retrieval Augmented Generation)**, usando políticas internas em PDF.
- Orquestrar fluxos de decisão com **grafo de agentes** (LangGraph).

---

## 🔨 Funcionalidades do Projeto

- **Aula 01** – Integração com Gemini API e criação de um modelo de **triagem**.
- **Aula 02** – Implementação de **RAG** com PDFs internos.
- **Aula 03** – Orquestração com **LangGraph**.
- **Masterclass_Python.ipynb** – Introdução ao Python (listas, dicionários, funções, tipos, boas práticas).

---

### 📸 Exemplo Visual do Projeto
	
<div align="center">
  <img width="415" height="480" alt="output" src="https://github.com/user-attachments/assets/6ab011a6-3e7b-412c-9523-e7378165bcd3" />
</div>

---

## ✔️ Técnicas e Tecnologias Utilizadas

- **Python 3.11+**
- **Google Generative AI (Gemini API)**
- **LangChain** e **LangGraph**
- **FAISS** – indexação vetorial
- **PyMuPDF** – leitura de PDFs
- **Pydantic** – validação de saída estruturada
- **Google Colab / Jupyter Notebook**

---

## 📁 Estrutura do Projeto

- **LICENSE** – Licença Apache 2.0  
- **Masterclass_Python.ipynb** – Notebook introdutório de Python  
- **Project.ipynb** – Notebook principal (Aulas 01–03)  
- **rag/** – PDFs usados no RAG:
  - `Política de Reembolsos (Viagens e Despesas).pdf`
  - `Política de Uso de E-mail e Segurança da Informação.pdf`
  - `Políticas de Home Office.pdf`

---

## 🛠️ Abrir e rodar o projeto

### 🔹 No Google Colab
1. Abra `Project.ipynb`.
2. Defina a variável `GEMINI_API_KEY` no ambiente do Colab (`userdata`) ou insira manualmente.
3. Faça upload dos PDFs da pasta `rag/` para `/content`.
4. Execute as células das aulas em ordem.

### 🔹 Localmente (Jupyter)
1. Instale as dependências:
   ```bash
   pip install langchain langchain-google-genai google-generativeai \
               langchain_community langchain-text-splitters faiss-cpu pymupdf \
               langgraph pydantic

2. Configure sua API Key do Gemini:

   * Crie um arquivo `.env`:

     ```
     GEMINI_API_KEY=sua_chave_aqui
     ```
3. Ajuste o caminho dos PDFs para `./rag`.
4. Execute o notebook `Project.ipynb`.

---

## 🌐 Deploy

* **Streamlit ou FastAPI** – expor agentes como API ou interface.
* **Docker** – empacotar dependências e notebooks.
* **Google Colab** – rodar diretamente sem instalação local.

---

## 📌 Observações

* O uso da **Gemini API** pode gerar custos dependendo do volume de requisições.
* Ao rodar localmente, considere **persistir o índice FAISS** em disco para evitar reprocessamento.
* Não versione chaves de API (`.env` deve estar no `.gitignore`).

📌 **Link de referência do guia oficial da imersão**:  
[Guia de Mergulho - Imersão Agentes de IA - Alura](https://alura.tv/guiademergulhoAgentesdeIA)



