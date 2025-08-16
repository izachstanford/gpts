# QuotebookGPT 📖✨

QuotebookGPT is a custom GPT that helps you **recall and explore
insights from books, talks, and articles you've collected over time**.\
It connects to your personal quote library (stored in Google Sheets) and
makes it easy to surface wisdom on demand.

![QuotebookGPT Main Interface](images/quotebookgpt-main.png)

*The QuotebookGPT main interface showing the book stack icon, title, description, and conversation starter buttons.*

------------------------------------------------------------------------

## 🚀 What It Does

-   Lets you search for quotes by **topic, author, or source**\
-   Defaults to a **vector-style search column** (`vector_search`) for
    best matching\
-   Always prioritizes high-rated quotes, but keeps results varied to
    surface new gems\
-   Lets you append new quotes directly into your inbox sheet (with
    Google OAuth)\
-   Lightweight and easy to extend for your own knowledge base

------------------------------------------------------------------------

## 🛠 How It Was Built

QuotebookGPT is powered by: - **Google Sheets** for storage\
- **Custom Actions** to fetch and write quotes: - `getPublicQuotes`:
fetches from the `ReadView` tab via GViz JSON (no auth required)\
- `appendQuoteToInbox`: appends quotes to the Inbox (auth required,
limited to the owner)\
- **System Recipe** (`recipe_quotebookgpt.md`) that guides GPT on how to
query, rank, and return quotes\
- **Markdown Docs**: - `privacy_policy.md` for GPT Store compliance\
- This README so others can replicate the approach\
- **Sample Data Template** (`Sample Template for QuotebookGPT.xlsx`) to
jump-start your own quotebook

------------------------------------------------------------------------

## 📂 Repository Structure

    /gpts/QuotebookGPT
    │── privacy_policy.md
    │── recipe_quotebookgpt.md
    │── README.md  👈 you are here
    │── Sample Template for QuotebookGPT.xlsx

------------------------------------------------------------------------

## 📝 How to Create Your Own QuotebookGPT

1.  **Copy the Template**
    -   Start with `Sample Template for QuotebookGPT.xlsx`\
    -   Add your own quotes under the `ReadView` tab\
    -   Populate the `vector_search` column with concatenated text for
        easier matching
2.  **Set Up Google Sheets**
    -   Import your Excel file into Google Sheets\
    -   Create two sheets:
        -   `ReadView` (for all quotes)\
        -   `Inbox` (for new submissions)
3.  **Create GPT**
    -   Use the `recipe_quotebookgpt.md` file as your system prompt\
    -   Adjust to your liking (e.g., change ranking, cap results, etc.)

![QuotebookGPT Configuration](images/quotebookgpt-config.png)

*The QuotebookGPT configuration interface showing the system prompt, conversation starters, and knowledge setup.*

4.  **Configure Actions**
    -   Add a `getPublicQuotes` action (GViz JSON endpoint, no auth)\
    -   Add an `appendQuoteToInbox` action (Google Sheets API with
        OAuth)

![Actions Configuration](images/actions-config.png)

*The Actions configuration panel showing Google services integration with docs.google.com and sheets.googleapis.com endpoints.*

5.  **Publish**
    -   Add a `privacy_policy.md` (required if you plan to share the link with friends and family)\
    -   Optional: add `terms_of_use.md` for completeness\
    -   Share with others!

------------------------------------------------------------------------

## 🧩 Extending It

You can easily modify this setup to:\
- Build a family sayings book\
- Create a leadership quote index\
- Capture research notes and resurface them later\
- Host any knowledge base that benefits from **smart recall with
randomness**

------------------------------------------------------------------------

## ⚖️ License & Attribution

This project is meant as a **personal knowledge tool** template. Feel
free to adapt it, but credit back if you publish your own.

------------------------------------------------------------------------

Happy quoting! ✨