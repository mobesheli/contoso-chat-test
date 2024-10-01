FROM  python:3.11-slim

WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
#copy product folder
COPY ./contoso_chat/ /app/contoso_chat
COPY ./contoso_chat/product /app
COPY . .

EXPOSE 80

CMD ["fastapi", "run", "main.py", "--port", "80"]
