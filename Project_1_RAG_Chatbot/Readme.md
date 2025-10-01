# 📘 Project 1: Document-Based Retrieval-Augmented Generation (RAG) Chatbot

## 🔍 Business Case

Companies spend a significant amount of time searching for information in user manuals, contracts, annual reports, and internal procedures. A RAG chatbot can:

- Reduce search time from minutes to seconds. The user asks a natural language question and receives a precise answer with a source reference.
- Improve the quality and consistency of support and knowledge sharing — the same model gives the same answer every time.
- Enable efficient customer support & free up expert hours: Technicians can focus on complex tasks instead of basic document questions, and support agents can quickly search for answers.
- Scalable: Whether you upload 1 or 10,000 pages, response time remains consistent thanks to an optimized vector index.
- Supports multilingual content (Danish, English, German) → matches the chain's geographic structure.
- **Limitation:** Uploading documents for the first time requires some patience.
<img width="541" height="240" alt="image" src="https://github.com/user-attachments/assets/059140b3-fb98-4425-b567-b5c138e6d515" />

---

## 🎯 Relevance Across Organizations

This solution can benefit a wide range of organizations by:

- Enabling fast and intelligent search across internal documentation (e.g., policies, product manuals, training materials), reducing time spent searching and increasing knowledge accessibility.
- Centralizing and standardizing knowledge across departments, regions, or teams — critical for ensuring alignment and quality.
- Supporting digital transformation goals by integrating AI-powered assistance into daily workflows.
- Reducing onboarding time for new employees by giving them direct access to structured internal knowledge.

---

## 🧩 Key Libraries and Tools Used

- **[Docling](https://docling-project.github.io/docling/):**
  - Parses PDFs/Word into markdown for better structure.
- **Pandas:**
  - Python library for data structuring, used to improve readability of tables extracted from markdown.
- **LangChain:**
  - Framework for building LLM-based applications.
- **Chroma:**
  - Local vector store for fast semantic search.
- **RecursiveCharacterTextSplitter:**
  - Splits long documents into manageable chunks so the LLM can better understand context.
- **OpenAI API:**
  - GPT model used to generate final answers based on document content.

---

## 💬 Example Prompts and Answers

```text
🔍 Ask a question about the annual report (or type 'exit'): What was Carlsberg's revenue in 2023?
💬 Answer: Carlsberg's revenue in 2023 was DKK 73,585 million.

🔍 Ask a question about the annual report (or type 'exit'): How much did their profit change from 2023 to 2024?
💬 Answer: For Carlsberg A/S, net profit changed from -DKK 40,788 million in 2023 to DKK 9,116 million in 2024. This represents an increase of DKK 49,904 million from 2023 to 2024.

🔍 Ask a question about the annual report (or type 'exit'): I need to present the document to a competing company. Tell me the key points such as vision, strategies, 2030 goals, and key financials. Limit to 1000 characters.
💬 Answer: The company's vision is to lead in sustainable beer production and create shareholder value. Strategic focus areas include innovation, environmentally friendly processes, and global growth. By 2030, the goal is to reduce CO2 emissions by 50% and increase market share by 15%. Key financials include growth in net profit, invested capital, and market share. The stock price is rising, and market capitalization is growing. A targeted payout ratio of 49% ensures consistent returns to shareholders.

🔍 Ask a question about the annual report (or type 'exit'): Are they satisfied with 2024?
💬 Answer: Yes, Carlsberg Group is satisfied with 2024, as they announced an expansion of their partnership with PepsiCo into four new markets. The expanded partnership makes Carlsberg Group the largest partner for PepsiCo in Europe and one of the largest globally. This collaboration is expected to bring long-term opportunities for both companies. Additionally, they emphasize consistent dividend payments, targeting a payout ratio of around 50% of adjusted net income. The proposed dividend for 2024 is DKK 27.0 per share, equivalent to an adjusted payout ratio of 49%.

🔍 Ask a question about the annual report (or type 'exit'): exit
