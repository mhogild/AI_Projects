# 🗞️ Project 2 – Personal AI News Assistant

## 🔍 Business Case

Automated news collection and personalized daily summaries.

While collecting news/emails/updates from various sources is not technically challenging (and is increasingly supported by tools like Microsoft Copilot), the real challenge was improving the *relevance* of what is collected using machine learning.

This project automates daily news aggregation and filtering to deliver 3 personally relevant AI-related news stories to the user every morning. The goal is for the assistant to continuously improve its relevance using user feedback and machine learning.

This eliminates the need for the user to browse multiple websites and sources — everything comes from a single, intelligent feed.

---

## 🎯 Relevance Across Organizations and Generations

This AI-powered assistant delivers:

- **Personalized news collections** based on interests like market trends, sustainability, industry updates, or tech innovation — valuable for managers, students, professionals, and curious learners.
- **Streamlined knowledge sharing**, enabling teams, departments, or families to access curated highlights without wasting time searching through irrelevant sources.

The tool fits both younger, tech-savvy users who want fast overviews, and older generations who prefer simplified and focused information.

---

## 🔄 Zapier Workflow (Zap A)

Below is a brief explanation of the automation:

![Zapier Flow – Zap A](./Projekt-2-Personlig-AI-Nyhedsassistent/zap_a_flow.png)

| Step | Tool                    | Function                                                         |
|------|--------------------------|------------------------------------------------------------------|
| 1    | **RSS by Zapier**        | Monitors multiple RSS feeds for new AI-related articles.         |
| 2    | **Formatter by Zapier**  | Formats and stores the current date.                             |
| 3    | **Google Sheets**        | Stores each news item (title, description, link, date).          |

---

## 🔁 Zapier Workflow (Zap B)

| Step | Tool                      | Function                                                                 |
|------|---------------------------|--------------------------------------------------------------------------|
| 1    | **Schedule by Zapier**    | Runs once daily (e.g., 07:00).                                           |
| 2    | **Formatter (date)**      | Identifies "yesterday" as the filter target.                            |
| 3    | **Google Sheets**         | Retrieves all news from yesterday using the stored data.                |
| 4    | **Formatter (utilities)** | Prepares and cleans up data formatting.                                 |
| 5    | **Filter**                | Filters rows to include only those from the previous day.               |
| 6    | **Formatter**             | Bundles title, description, and feedback for the prompt.                |
| 7    | **ChatGPT (OpenAI)**      | Sends the full list (raw and filtered) to GPT-4 for summarization.      |
