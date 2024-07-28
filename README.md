
# Тестовое задание: Хонипот на базе OpenCanary

## Описание
Проект демонстрирует настройку и модификацию хонипота OpenCanary для имитации страницы входа RabbitMQ. Включает установку и настройку OpenCanary и RabbitMQ, изменение внешнего вида OpenCanary для отображения интерфейса RabbitMQ, а также проверку работы хонипота. 

Осуществляются следующие шаги:
1. Настройка виртуальной машины.
2. Установка и настройка OpenCanary и RabbitMQ.
3. Изменение внешнего вида OpenCanary для имитации страницы RabbitMQ.
4. Проверка работы хонипота.

## Установка и запуск

### 1. Подготовка виртуальной машины

### 2. Установка OpenCanary
1. Клонирование репозитория:      
git clone https://github.com/thinkst/opencanary.git   
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

### 4. Получение HTML, CSS и JS страниц RabbitMQ

### 5. Модификация OpenCanary
1. Изменение HTML, CSS и JavaScript в OpenCanary для имитации интерфейса RabbitMQ:
   - Изменить HTML шаблоны в OpenCanary для отображения страницы входа RabbitMQ.   - Обновить CSS и JavaScript для стилизации и функциональной интеграции внешнего вида RabbitMQ.
2. Перезапуск OpenCanary для применения изменений:
opencanaryd --start
      

## Выводы
Реализован хонипот на базе OpenCanary, имитирующий страницу входа RabbitMQ. Все необходимые модули настроены, интерфейс изменен в соответствии с требованиями. Проверена работа хонипота и его способность фиксировать входящие попытки и события.

