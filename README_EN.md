# AI agnet immersion

**Masterclass**  
- https://guilhermeonrails.github.io/materclass-python-ia-agentes/#cap5  
- https://fiapcom.sharepoint.com/sites/Alura/Documents/Forms/AllItems.aspx?id=%2Fsites%2FAlura%2FDocuments%2FAlura%20%5F%20Growth%2F2%2E%20Product%20Marketing%2FCompartilhados%20externos%2FImers%C3%A3o%20Dev%20Agentes%20IA%2FPython%2DMasterclass%201%2Epdf&parent=%2Fsites%2FAlura%2FDocuments%2FAlura%20%5F%20Growth%2F2%2E%20Product%20Marketing%2FCompartilhados%20externos%2FImers%C3%A3o%20Dev%20Agentes%20IA&p=true&ga=1  

**Google API Key**  
- https://aistudio.google.com/app/apikey  

**Download PDFs used in the class**  
- https://fiapcom.sharepoint.com/sites/Alura/Documents/Forms/AllItems.aspx?id=%2Fsites%2FAlura%2FDocuments%2FAlura%20%5F%20Growth%2F2%2E%20Product%20Marketing%2FCompartilhados%20externos%2FImers%C3%A3o%20Dev%20Agentes%20IA%2FPDFs%20Aula%202&viewid=a4e246d8%2D2213%2D4b9d%2D980e%2D02833d082636&ga=1  

---

# AI-Agent-Immersion

This repository contains materials and notebooks from the **AI Agents Immersion**, covering everything from basic Python concepts to building intelligent agents using **LangChain**, **Google Gemini**, and **LangGraph**.

The goal is to implement a **Service Desk agent** capable of:
- Automatically classifying messages (structured triage).
- Answering questions using **RAG (Retrieval Augmented Generation)** with internal PDF policies.
- Orchestrating decision flows with an **agent graph** (LangGraph).

---

## 🔨 Project Features

- **Lesson 01** – Gemini API integration and building a **triage** model.  
- **Lesson 02** – **RAG implementation** with internal PDFs.  
- **Lesson 03** – **Agent orchestration** with LangGraph.  
- **Masterclass_Python.ipynb** – Python introduction (lists, dictionaries, functions, types, best practices).  

---

### 📸 Visual Example of the Project
	
<div align="center">
  <img width="415" height="480" alt="output" src="https://github.com/user-attachments/assets/6ab011a6-3e7b-412c-9523-e7378165bcd3" />
</div>

---

## ✔️ Technologies and Tools Used

- **Python 3.11+**
- **Google Generative AI (Gemini API)**
- **LangChain** and **LangGraph**
- **FAISS** – vector index
- **PyMuPDF** – PDF parsing
- **Pydantic** – structured output validation
- **Google Colab / Jupyter Notebook**

---

## 📁 Project Structure

- **LICENSE** – Apache 2.0 License  
- **Masterclass_Python.ipynb** – Python introductory notebook  
- **Project.ipynb** – Main notebook (Lessons 01–03)  
- **rag/** – PDFs used for RAG:
  - `Política de Reembolsos (Viagens e Despesas).pdf`
  - `Política de Uso de E-mail e Segurança da Informação.pdf`
  - `Políticas de Home Office.pdf`

---

## 🛠️ Running the Project

### 🔹 On Google Colab
1. Open `Project.ipynb`.  
2. Set the `GEMINI_API_KEY` variable in Colab environment (`userdata`) or manually.  
3. Upload the PDFs from the `rag/` folder to `/content`.  
4. Run the lesson cells in order.  

### 🔹 Locally (Jupyter)
1. Install dependencies:
   ```bash
   pip install langchain langchain-google-genai google-generativeai \
               langchain_community langchain-text-splitters faiss-cpu pymupdf \
               langgraph pydantic
````

2. Configure your Gemini API Key:

   * Create a `.env` file:

     ```
     GEMINI_API_KEY=your_key_here
     ```
3. Adjust the PDF path to `./rag`.
4. Run the `Project.ipynb` notebook.

---

## 🌐 Deployment

* **Streamlit or FastAPI** – expose agents as API or interface.
* **Docker** – package dependencies and notebooks.
* **Google Colab** – run directly in the cloud without local setup.

---

## 📌 Notes

* Using the **Gemini API** may incur costs depending on usage volume.
* When running locally, consider **persisting the FAISS index** to disk to avoid reprocessing.
* Do not commit API keys (`.env` must be in `.gitignore`).
