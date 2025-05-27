# Инструкция по развертыванию видеоплатформы

##  Требования к системе
- Python 3.8+
- pip (менеджер пакетов Python)
- SQLite3 (обычно входит в состав Python)
- Доступ в интернет (для установки зависимостей)

## 🛠 Установка зависимостей

1. Клонируйте репозиторий:
```bash
git clone https://github.com/Darkness1853/programming-JavaScript.git
cd programming-JavaScript/Project/video-platform
```

2. Установите необходимые пакеты:
```bash
pip install flask flask-sqlalchemy flask-jwt-extended flask-bcrypt werkzeug
```

##  Настройка приложения

1. Создайте необходимые директории:

##  Запуск приложения

### Локальный запуск (для разработки)
```bash
python main.py или python3 main.py ( зависит от версии python)
```
Приложение будет доступно по адресу: `http://127.0.0.1:5000`

### Публичный доступ через Serveo
```bash
ssh -R 80:localhost:5000 serveo.net
Или если есть личный домен самостоятельно создать
```
После выполнения команды вы получите публичный URL вида: `https://<поддомен>.serveo.net`

## 🔄 Инициализация базы данных
При первом запуске автоматически создается файл `instance/site.db`. 
Для сброса базы данных:
```bash
rm -f instance/site.db
python init_db.py
```

## Структура проекта
```
video-platform/
├── main.py            # Основное приложение
├── templates/         # HTML шаблоны
├   ├──base.html
├   ├──index.html
├   ├──login.html
├   ├──register.html
├   ├──upload.html
├   ├──video.html
├── videos/            # Загруженные видео
└── instance/          # База данных
```
