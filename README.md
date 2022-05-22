 ![image](https://user-images.githubusercontent.com/105894189/169672950-caf20cb9-26d5-4c4e-9ff0-54ccef2756ea.png)

### Маршрутизатор базується на докерах, тому його можна запускати з багатьма підходами. Цей посібник буде зосереджено на тих, хто працює на сервері Ubuntu.

#### Для цього нам знадобиться:
   
  - Ubuntu сервер
   
   > У цьому посібнику я використовую сервер Ubuntu 20.04
  
  - Docker 20.10.5 або новіше

  - Docker Compose 1.27.4 або новіше
 
 ### Почнемо
 
  - Клонуйте маршрутизатор docker-compose на свій сервер
  
        git clone https://github.com/connext/nxtp-router-docker-compose
        cd nxtp-router-docker-compose/
        git checkout amarok

  - Створення конфіга змінних
  
         cp .env.example .env
         sudo nano.env
        
       >Тут потрібно змінити версію маршрутизатора. Ви можете знайти її тут https://github.com/connext/nxtp/releases
    
  - Тепер створюємо конфіг файл
  
         sudo nano config.json

       - після  «logLevel»: «debug»,  введіть наступне,
       
             «mnemonic»: «seed phrase»,
       - і вставте замість "seed phrase" вашу справжню фразу від гаманця маршрутизатора

### Запуск маршрутизатора

    sudo docker-compose up -d
    
## Останній код

    docker-compose logs router
    
# Мої вітання!
