FROM python:3.12-slim

WORKDIR /translator-app

# Copy only requirements.txt first to leverage Docker's caching (Check out image layering)
COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 7860

CMD ["python", "main.py"]