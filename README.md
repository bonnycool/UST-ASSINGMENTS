python -c "import chromadb; c=chromadb.PersistentClient(path='data/vector_store'); print([(x.name,x.count()) for x in c.list_collections()])"
