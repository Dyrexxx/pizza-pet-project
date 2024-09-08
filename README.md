# pizza-pet-project
Стек:
  1. java 17
  2. mapstruct
  3. thymeleaf
  4. liquibase
  5. docker
  6. postgreSQL

     
Перед запуском убедительная просьба иметь в доступе пустые базы данных на порту 5432:
  1. restaurant-dev
  2. products-dev
  3. maker-menu-dev


Склонировать проект
1. git clone https://github.com/Dyrexxx/pizza-pet-project.git
2. Перейти в общую директорию проекта
3. cd pizza-pet-project/
4. Добавить файлы для подмодулей
5. git submodule update --init --recursive
6. Обновить подмодули из удаленного репозитория
7. git submodule update --remote

Запуск через dockerCompose:
1. Перейти в общую директорию pizza-pet-project
2. mvnw clean package dockerfile:build
3. cd docker/
4. docker-compose up -d

Обычный запуск:
1. Открыть общую директорию проекта через idea
2. Запустить spring boot:
   ![image](https://github.com/user-attachments/assets/762a93bf-2629-4316-8d1b-e339c2f11c57)

Документация Swagger api и dto http://localhost:8085/swagger-ui/index.html



