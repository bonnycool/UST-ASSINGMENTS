$env:HF_HOME = "$env:USERPROFILE\.cache\huggingface"
python -m streamlit run app.py --server.address 127.0.0.1 --server.fileWatcherType none
