FROM python:3.11-slim

# Устанавливаем рабочую директорию
WORKDIR /server

# Копируем зависимости и устанавливаем их
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Копируем код приложения
COPY app.py .

# Запускаем FastAPI приложение
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8000"]
