Write-Host "===== PYTHON ====="
python --version

Write-Host "===== GEMINI KEY ====="
python -c "from dotenv import load_dotenv; load_dotenv(); import os; print('Key available:', bool(os.getenv('GEMINI_API_KEY')))"

Write-Host "===== CHROMA DATABASE ====="
python -c "import chromadb; c=chromadb.PersistentClient(path='data/vector_store'); print([(x.name,x.count()) for x in c.list_collections()])"

Write-Host "===== EMBEDDING MODEL ====="
python -c "from sentence_transformers import SentenceTransformer; m=SentenceTransformer('all-MiniLM-L6-v2',local_files_only=True); print('Embedding model loaded successfully')"

Write-Host "===== INCIDENT FILES ====="
Get-ChildItem data\incidents

Write-Host "===== CHECKS COMPLETE ====="
