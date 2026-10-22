Get-ChildItem src -Recurse -Filter *.py | Select-String -Pattern 'embedding_model|EMBEDDING_MODEL|all-MiniLM|persist_directory|chroma_path' | Select-Object -First 25 Path,LineNumber,Line
