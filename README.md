
# Тестовое задание: Ханипот на базе OpenCanary

## Описание
Проект демонстрирует настройку и модификацию ханипота OpenCanary для имитации страницы входа RabbitMQ. Включает установку и настройку OpenCanary и RabbitMQ, изменение внешнего вида OpenCanary для отображения интерфейса RabbitMQ, а также проверку работы ханипота. 

Осуществляются следующие шаги:
1. Настройка виртуальной машины.
2. Установка и настройка OpenCanary и RabbitMQ.
3. Изменение внешнего вида OpenCanary для имитации страницы RabbitMQ.
4. Проверка работы ханипота.

## Установка и запуск

### 1. Подготовка виртуальной машины

### 2. Установка OpenCanary
1. Клонирование репозитория:      
git clone https://github.com/LiOmr/honeypot-project  
cd opencanary
   
2. Создание и активация виртуального окружения:      
python3 -m venv venv   
source venv/bin/activate
   
3. Установка зависимостей:      
pip install -r requirements.txt   

4. Установка OpenCanary:
pip install .
      
5. Создание конфигурационного файла:
opencanaryd --copyconfig
      
6. Редактирование конфигурационного файла 
/etc/opencanaryd/opencanary.conf для включения HTTP/HTTPS модулей.

### 3. Установка RabbitMQ
1. Добавление репозитория RabbitMQ:      
sudo apt-get update   
sudo apt-get install -y erlang
sudo apt-get install -y rabbitmq-server   
2. Запуск RabbitMQ:
sudo systemctl enable rabbitmq-server   

### 4. Модификация OpenCanary
1.Перезапуск OpenCanary для применения изменений:
opencanaryd --start
      



