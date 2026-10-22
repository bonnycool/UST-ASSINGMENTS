@'
from sentence_transformers import SentenceTransformer
SentenceTransformer("all-MiniLM-L6-v2", local_files_only=True)
print("MODEL LOADED SUCCESSFULLY")
'@ | python -
