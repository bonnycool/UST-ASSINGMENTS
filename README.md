Select-String -Path src\config.py -Pattern "EMBEDDING_MODEL_NAME" | ForEach-Object { $_.Line }
