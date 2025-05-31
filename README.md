# 🗃️ Chat with SQL DB Dynamically

This project is a **Streamlit-based AI assistant** that lets you chat with your SQL database using **natural language**. It uses **LangChain** and **Groq's LLaMA3 model** to understand and convert user input into SQL queries, offering powerful insights from your database — whether it's a local SQLite file or a remote MySQL database.

---

## 📁 Project Contents

- `app.py`: Main Streamlit app to query the database with natural language  
- `sqlite.py`: Script to initialize and populate the SQLite database (`pr_report.db`)  
- `pr_report.db`: Preloaded SQLite database with purchase request data

---

## ⚙️ Key Features

- 🔍 Natural language interface for querying a database  
- 💬 Real-time chat with conversational history  
- 🧠 Powered by LangChain + Groq LLaMA3 (via API key)  
- 🗃️ Supports both SQLite and MySQL connections  
- 🧩 Modular and extensible for any kind of database schema  

---

## 🧪 Sample Data Overview (`prreport` Table)

| pr_id | requested_by | location     | product_name | product_id | approved_by | vendor         | approval_status |
|-------|--------------|--------------|--------------|------------|-------------|----------------|------------------|
| 001   | Thirumurugan | koramangala  | apple        | 01         | siddharth   | insfusion      | 1                |
| 002   | Sagar        | Nexus mall   | orange       | 02         | madhushree  | ffservices     | 1                |
| 003   | Thirumurugan | rich street  | pineapple    | 03         | sagar       | ananya shelter | 1                |
| 004   | madhushree   | koramangala  | watermelon   | 04         | Thirumurugan| devalt         | 1                |
| 005   | krishna      | madiwala     | grapes       | 05         |             | zepto          | 0                |
| 006   | Thirumurugan | koram        | grapes       | 05         |             | gssprojects    | 0                |
| 007   | Krishna      | bommanahalli | apple        | 06         |             | insfusion      | 0                |

---

## 🚀 Getting Started

### Step 1: Install Required Packages

```bash
pip install streamlit langchain langchain-community langchain-groq sqlalchemy mysql-connector-python
Step 2: Set Up the Database (Optional)
To recreate the SQLite DB from scratch, run:

bash
Copy
Edit
python sqlite.py
This creates the pr_report.db file and inserts sample purchase requests.

Step 3: Launch the Streamlit App
bash
Copy
Edit
streamlit run app.py
🛠️ How It Works
✅ Sidebar Options
Use SQLite 3 Database – pr_report.db (default)

Connect to your MySQL database (custom)

✅ Input Required
Groq API Key (required to use LLaMA3 via LangChain)

For MySQL: host, user, password, and database name

✅ Example Questions to Ask
"Show all approved purchase requests"

"List requests from Thirumurugan"

"What is the vendor for product ID 03?"

"Which requests are still pending approval?"

🧾 How sqlite.py Works
Connects to SQLite

Defines prreport table structure (commented out)

Inserts sample data

Prints all rows where approval_status = 1

🧾 How app.py Works
Streamlit interface with sidebar for DB & API setup

Uses LangChain's create_sql_agent with ChatGroq LLM

Connects to SQLite or MySQL based on selection

Caches DB connection for 2 hours

Maintains message history between questions

Displays assistant responses via chat interface

📌 Notes
Ensure pr_report.db is in the same directory as app.py

Groq API key is required and securely entered via sidebar

You can clear chat history anytime with the sidebar button

🧩 Sample requirements.txt
txt
Copy
Edit
streamlit
langchain
langchain-community
langchain-groq
sqlalchemy
mysql-connector-python
📄 License
MIT License – free to use, modify, and distribute.

🙋‍♂️ Want More?
If you want to:

Add file upload (CSV to DB)

Support PostgreSQL or Oracle

Deploy on Streamlit Cloud or Hugging Face

Add user authentication

Let me know and I can help you extend it!

yaml
Copy
Edit

---

Let me know if you want this as a downloadable `README.md` file too!






