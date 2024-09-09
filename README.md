# Итоговый проект "Пицца Хаус"
**Стек:**
  > 1. java 17
  > 2. mapstruct
  > 3. thymeleaf
  > 4. liquibase
  > 5. docker
  > 6. postgreSQL

**Схема взаимодействия микросервисов (gateway, courier на данный момент до конца не реализованы, поэтому не включены в проект):**
<br>
![image](https://github.com/user-attachments/assets/77459a7b-3be4-4424-9980-1c0b47cf01d9)


     
**Перед запуском убедительная просьба иметь в доступе пустые базы данных на порту 5432:**
  > 1. restaurant-dev
  > 2. products-dev
  > 3. maker-menu-dev


**Склонировать проект**
1. git clone https://github.com/Dyrexxx/pizza-pet-project.git
**Перейти в общую директорию проекта**
2. cd pizza-pet-project/
**Добавить файлы для подмодулей**
3. git submodule update --init --recursive
**Обновить подмодули из удаленного репозитория**
4. git submodule update --remote

**Запуск через dockerCompose:**
> 1. Перейти в общую директорию pizza-pet-project
> 2. mvnw clean package dockerfile:build
> 3. cd docker/
> 4. docker-compose up -d

**Обычный запуск:**
> 1. Открыть общую директорию проекта через idea
> 2. Запустить spring boot:
   ![image](https://github.com/user-attachments/assets/762a93bf-2629-4316-8d1b-e339c2f11c57)

**Документация Swagger api и dto** http://localhost:8085/swagger-ui/index.html

**Схемы бд:**
> 1. restaurant: ![image](https://github.com/user-attachments/assets/80c0b263-9a42-4957-9d69-f5be173c0911)
> 2. maker-menu: ![image](https://github.com/user-attachments/assets/f2bb6231-6817-4813-b9a2-df83a7b8e18e)
> 3. products: ![image](https://github.com/user-attachments/assets/1ef15371-6fdc-4a82-890c-8ac30ae3f0ea)




**Точки входа в микросервисы:**
  > 1. localhost:8081/site - GUI для пользователя, который хочет заказать еду на дом ![image](https://github.com/user-attachments/assets/911c4b5b-f40d-409e-82bc-e585ef479f1f)

  > 2. localhost:8083/maker - GUI для создателя меню. Здесь храняться данные о всех используемых ингредиентах. Есть возможность создать в меню новое блюдо ![image](https://github.com/user-attachments/assets/72372a42-6d4a-483b-a600-92fd7e162cae)

  > 3. localhost:8085/restaurant - GUI для действующих ресторанов. Здесь находиться склад с ингредиентами. Бд онлайн-заказов. Бд ожидание пополнения новых ингредиентов на склад ![image](https://github.com/user-attachments/assets/e0212cd5-c02d-46b7-a8a0-c7e8a356f729)

  > 4. localhost:8086/warehouses - GUI для создания новых доставок новых ингредиентов на склады ресторанов ![image](https://github.com/user-attachments/assets/140d1923-9979-452b-b9b5-c03784ea292b)




