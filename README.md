# 🦜 Chat with SQL Database using LangChain & Groq

An AI-powered SQL assistant built with **LangChain**, **Groq LLM**, **Streamlit**, and **SQLAlchemy** that enables users to interact with **SQLite** and **MySQL** databases using natural language.

Instead of writing SQL queries manually, simply ask questions in plain English, and the AI agent generates, executes, and explains SQL queries for you.

---

## 🚀 Features

- 💬 Chat with SQL databases using natural language
- 🗄️ Supports both **SQLite** and **MySQL**
- 🤖 Powered by **Groq Llama 3.1**
- 🔗 Uses LangChain SQL Agent for query generation
- ⚡ Interactive Streamlit interface
- 🧠 Displays the agent's reasoning process
- 🔍 Automatically understands database schema
- 📊 Returns SQL query results in an easy-to-read format

---

## 🛠️ Tech Stack

- Python
- Streamlit
- LangChain
- LangChain Community
- LangChain Groq
- SQLAlchemy
- SQLite
- MySQL
- MySQL Connector
- python-dotenv

---

## 📂 Project Structure

```
CHAT_WITH_SQLDB/
│
├── app.py
├── student.db
├── requirements.txt
├── .env
├── README.md
└── .gitignore
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Maaddhhaav21/CHAT_WITH_SQLDB.git

cd CHAT_WITH_SQLDB
```

---

### 2. Create a Virtual Environment

Using **uv**

```bash
uv venv .venv --python 3.11 --seed
source .venv/bin/activate
```

or using Python

```bash
python -m venv .venv
source .venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

or

```bash
uv pip install -r requirements.txt
```

---

## 🔑 Configure Groq API Key

Create a `.env` file:

```env
GROQ_API_KEY=your_groq_api_key
```

Or enter your API key directly in the Streamlit sidebar.

Get your API key from:

https://console.groq.com/keys

---

## ▶️ Run the Application

```bash
python -m streamlit run app.py
```

---

## 🗄️ Supported Databases

### SQLite

Uses the included `student.db` database.

### MySQL

Provide:

- Host
- Username
- Password
- Database Name

The application will automatically connect using SQLAlchemy.

---

## 💡 Example Questions

SQLite

- Show all students.
- List students with grade A.
- How many students are in the database?
- Display students sorted by marks.
- Who scored the highest marks?

MySQL

- Show all employees.
- List customers from London.
- Find the total sales.
- Show the top 5 products.
- Count the number of orders.

---

## 🧠 How It Works

1. User enters a natural language question.
2. LangChain SQL Agent understands the database schema.
3. The agent generates an SQL query.
4. SQLAlchemy executes the query.
5. Results are returned to the LLM.
6. Groq Llama generates a human-readable response.
7. Streamlit displays both the reasoning process and the final answer.

---

## 📸 Demo

Example:

**User**

> Show all students with Grade A.

**Agent**

```sql
SELECT * FROM STUDENT
WHERE GRADE='A';
```

**Response**

Returns all students who have secured Grade A.

---

## 📦 Requirements

- Python 3.11
- Groq API Key
- Internet Connection

---

## 🔮 Future Improvements

- PostgreSQL support
- SQL Server support
- Database upload feature
- Query history
- Authentication
- Chat memory
- CSV/Excel export
- Docker deployment

---

## 👨‍💻 Author

**Madhav Manoj**

GitHub:
https://github.com/Maaddhhaav21


## 📄 License

This project is intended for educational and learning purposes.
