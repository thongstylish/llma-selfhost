cp llama-selfhost
docker build -f Dockerfile -t thong-llama-server .

docker run -d -v /root/Llama-3.1-8B-UltraLong-4M-Instruct-GGUF:/models \
           -p 8000:8000 \
           thong-llama-server:latest \
           -m /models/Llama-3.1-8B-UltraLong-4M-Instruct-Q6_K.gguf \
           --port 8000 \
           --host 0.0.0.0 \
           -n 512

/Llama-3.1-8B-UltraLong-4M-Instruct-GGUF# tree
.
├── Llama-3.1-8B-UltraLong-4M-Instruct-Q3_K_L.gguf
├── Llama-3.1-8B-UltraLong-4M-Instruct-Q6_K.gguf
├── Llama-3.1-8B-UltraLong-4M-Instruct-Q8_0.gguf
└── README.md
