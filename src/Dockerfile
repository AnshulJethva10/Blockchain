FROM python:3.9-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY blockchain.py .
COPY index.html .

# Expose ports for both the API and web server
EXPOSE 5000 8000

# Start both services
CMD ["sh", "-c", "python -m http.server 8000 & python blockchain.py --port 5000"]