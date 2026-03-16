# QA Automation

форк "автоматизированное тестирование UI на базе Selenium Grid + pytest."

## Стек
- Python 3.11
- Selenium 4 + Selenium Grid
- pytest 
- Docker / docker-compose
- GitHub Actions (self-hosted runner)
- Prometheus + Grafana

## Запуск

Поднять Selenium Grid:
```bash
docker run -d -p 4444:4444 -p 7900:7900 selenium/standalone-chrome:latest
```

Запустить тесты:
```bash
docker build -t test .
docker run --network selenium-net test:latest
```

Мониторинг:
```bash
cd monitoring
docker-compose up -d
```
Grafana: 31.130.149.55:3000


k3s/hadoop soon 
