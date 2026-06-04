# 🛒 MultiModal AI Shopping Assistant Agent

An intelligent shopping assistant built using **LangChain Agents, Groq LLMs, Vision AI, SQLite, and Streamlit**. The assistant can understand natural language shopping requests, retrieve product ratings, analyze uploaded product images, recommend suitable products, and complete purchases through an agentic tool-calling workflow.

---

## 📌 Project Overview

Modern e-commerce platforms contain thousands of products, making product discovery difficult for users.

This project demonstrates how Large Language Models can be combined with external tools and databases to create an intelligent shopping assistant capable of:

* Understanding user shopping requirements
* Searching products using natural language
* Filtering products based on constraints
* Retrieving customer ratings
* Recommending the best products
* Analyzing uploaded product images
* Finding visually similar products
* Completing purchases through tool calling

The system uses a LangChain Agent that dynamically decides which tools to invoke based on user requests.

---

# 🚀 Features

### 🔍 Natural Language Product Search

Search products using conversational language.

Example:

```text
I want organic honey under $20 with rating above 4.5
```

The assistant automatically:

1. Searches products
2. Retrieves ratings
3. Filters results
4. Recommends suitable products

---

### ⭐ Product Rating Retrieval

Retrieve customer review statistics directly from the database.

Example:

```text
Show rating for product ID 5
```

Output:

```json
{
  "product_id": 5,
  "average_rating": 4.8,
  "review_count": 120
}
```

---

### 🖼️ Image-Based Product Search

Upload a product image and let the Vision LLM identify it.

The assistant:

1. Analyzes the image
2. Extracts product attributes
3. Searches the catalog
4. Returns similar products

---

### 🛍️ Intelligent Product Recommendations

Recommendations are generated based on:

* Product category
* Description
* Price constraints
* Organic preference
* Customer ratings

---

### 💳 AI-Powered Checkout

After user confirmation, the assistant:

1. Identifies the selected product
2. Places the order
3. Stores the transaction
4. Returns an order confirmation

---


# ⚙️ Technology Stack

| Component              | Technology    |
| ---------------------- | ------------- |
| Frontend               | Streamlit     |
| Agent Framework        | LangChain     |
| LLM                    | Groq          |
| Vision Model           | Llama 4 Scout |
| Database               | SQLite        |
| Backend                | Python        |
| Environment Management | python-dotenv |

---

# 🧠 Agent Workflow

## Product Search Flow

```text
User Query
    │
    ▼
Search Products Tool
    │
    ▼
Get Product Ratings
    │
    ▼
Apply Filters
    │
    ▼
Recommend Products
```

---

## Image Search Flow

```text
Upload Product Image
         │
         ▼
Vision LLM Analysis
         │
         ▼
Extract Product Attributes
         │
         ▼
Search Product Database
         │
         ▼
Recommend Similar Products
```

---

# 📂 Project Structure

```text
MultiModal-AI-Shopping-Assistant-Agent/
│
├── Trial_Images/
│   ├── honey.png
│   ├── oats.png
│   ├── elephant.png
│   └── gun.png
│
├── Streamlit.py          # Streamlit frontend application
├── shopping_agent.py     # LangChain agent and tools
├── get_reviews.py        # Product rating retrieval functions
├── store.db              # SQLite product, review, and order database
│
├── Requirements.txt      # Project dependencies
├── README.md             # Project documentation
├── LICENSE               # MIT License
└── .gitignore            # Ignored files and folders
```

---

# 🔧 Installation

## Clone Repository

```bash
git clone https://github.com/<your-username>/MultiModal-AI-Shopping-Assistant-Agent.git

cd MultiModal-AI-Shopping-Assistant-Agent
```

---

## Install Dependencies

```bash
pip install -r Requirements.txt
```

---

## Configure Environment Variables

Create a `.env` file:

```env
GROQ_API_KEY=your_groq_api_key
```

---

## Run Application

```bash
streamlit run Streamlit.py
```

---

# 💡 Example Queries

```text
I want organic honey under $20
```

```text
Show products rated above 4.5
```

```text
Find similar products to this image
```

```text
Order the first product
```

```text
I want organic almonds with rating above 4 stars
```

---

# 📈 Future Improvements

* Vector Database Integration
* Product Embedding Search
* RAG-based Product Knowledge
* Personalized Recommendations
* Shopping Cart Memory
* Inventory Management
* Multi-Vendor Marketplace Support
* Real-Time Product Availability
* Voice Shopping Assistant

---

# 🎯 Key Learning Outcomes

This project demonstrates:

* Agentic AI Workflows
* Tool Calling
* Function Calling with LLMs
* Multi-Step Reasoning
* Vision Language Models
* Database Integration
* LangChain Agents
* Streamlit Deployment
* Conversational AI Systems

---
