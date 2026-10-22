python -c "import chromadb; c=chromadb.PersistentClient(path='data/vector_store'); print([(x.name,x.count()) for x in c.list_collections()])"
echo ===== PYTHON =====
python --version

echo ===== GEMINI API KEY =====
python -c "from dotenv import load_dotenv; load_dotenv(); import os; print('Key available:', bool(os.getenv('GEMINI_API_KEY')))"

echo ===== CHROMA DATABASE =====
python -c "import chromadb; c=chromadb.PersistentClient(path='data/vector_store'); print([(x.name,x.count()) for x in c.list_collections()])"

echo ===== EMBEDDING MODEL =====
python -c "from sentence_transformers import SentenceTransformer; m=SentenceTransformer('all-MiniLM-L6-v2',local_files_only=True); print('Embedding model loaded successfully')"

echo ===== INCIDENT FILES =====
dir data\incidents

echo ===== CHECKS COMPLETE =====
