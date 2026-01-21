FROM python:3.12-alpine

WORKDIR /app

RUN addgroup -S app && adduser -S app -G app

COPY app.py /app/app.py

USER app

EXPOSE 8080

CMD ["python", "/app/app.py"]

