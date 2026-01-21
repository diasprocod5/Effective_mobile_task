### Для запуска проекта необходимы:  
Docker, Docker Compose (v2)

### Инструкция по запуску:

Загрузите репозиторий:   
`git clone https://github.com/diasprocod5/effective_mobile_task.git`  

Перейдите в загруженный каталог  
`cd effective_mobile_task`

Создайте файл .env на основе примера   
`cp .env.example .env`

Запустите docker compose  
`docker compose up -d --build`


### Проверка работоспособности:

`curl http://localhost`  
Ожидаемый ответ "Hello form Effective mobile"


### Архитектура проекта:
- Nginx принимает входящие HTTP-запросы на порт 80 и выступает в роли reverse proxy, перенаправляя все запросы к backend-сервису на  порт 8080.  

- Backend — HTTP-сервер на Python, слушающий порт 8080
и обрабатывающий запросы к корневому пути "/".  
Backend-сервис изолирован и недоступен напрямую с хоста.
