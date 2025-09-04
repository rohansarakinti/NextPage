# 📚 Book Recommender System  

A machine learning project to recommend books using **semantic similarity** over descriptions.  
The project also aims to **clean up noisy categories** using **zero-shot classification**.  

---

## 🚀 Features  

- **Data Exploration** (`data-exploration.ipynb`)  
  - Loads the Kaggle dataset `dylanjcastillo/7k-books-with-metadata`.  
  - Cleans and filters descriptions (≥ 25 words).  
  - Creates derived features like `age_of_book`.  
  - Exports `books_cleaned.csv`.  

- **Vector Similarity Search** (`vector-search.ipynb`)  
  - Converts book descriptions into embeddings with **OpenAI + LangChain**.  
  - Stores vectors in a **Chroma** index.  
  - Queries for semantically similar books.  
  - Outputs `tagged_description.txt`.  

- **Planned: Zero-Shot Classification**  
  - Use Hugging Face models to condense categories into meaningful groups (e.g. Fiction, Non-Fiction, Fantasy).  
  - Drop noisy or redundant categories.  

---

## 🗂 Project Structure  

```
.
├─ data-exploration.ipynb     # Download, clean, and profile the dataset
├─ vector-search.ipynb        # Embedding + similarity search with LangChain & Chroma
├─ README.md                  # Project documentation
└─ (generated at runtime)
   ├─ books_cleaned.csv
   └─ tagged_description.txt
```

---

## ⚙️ Installation  

All commands below are for **Windows CMD**.  

```cmd
:: 1. Clone the repo
git clone https://github.com/yourusername/book-recommender.git
cd book-recommender

:: 2. Create and activate virtual environment
python -m venv .venv
.\.venv\Scriptsctivate

:: 3. Install dependencies
pip install --upgrade pip
pip install -r requirements.txt

:: 4. Set your OpenAI API key (create .env file)
echo OPENAI_API_KEY=sk-your-key-here> .env

:: 5. Launch Jupyter
jupyter notebook
```

---

## 📦 Requirements  

Core dependencies:  

- `pandas`, `numpy` → Data handling  
- `matplotlib`, `seaborn` → Visualization  
- `kagglehub` → Download Kaggle datasets  
- `langchain`, `langchain-openai`, `langchain-community`  
- `chromadb` → Vector database  
- `python-dotenv` → API key management  
- `openai` → Embeddings  
- `transformers`, `torch` → Zero-shot classification (planned)  

---

## 📈 Next Steps  

- [ ] Add **zero-shot classification** notebook.  
- [ ] Evaluate recommendation quality.  
- [ ] Package as a pipeline.  
- [ ] Build a demo app (Streamlit/Flask).  

---

## 🤝 Contributing  

Pull requests and issues are welcome.  

---

## 📜 License  

This project is licensed under the MIT License.  
