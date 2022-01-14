Есть сущность диета, которая имеет определенный параметр key.
Всего есть три диеты: gentle_1200, gentle_1600, gentle_2000. Каждая имеет определенное дневное меню (список блюд).
Блюдо описывается полем name. Блюда с одинаковым названием идентичны во всех диетах.
Приложение представляет собой JSON API и обрабатывает 2 запроса:
 
 `POST /orders?diet_key={diet_key}` (например `/orders?diet_key=gentle_1200`) который создает заказ с определенной диетой.  
 
 `GET /dishes` выгружает ответ вида  `[ { name: 'Омлет с брокколи', count: 10 }, { name: 'Овсяный сырник с вишней', count: 9 }, ...]`
 count - количество блюд, которое надо приготовить, исходя из заказов. Массив ответа отсортирован в порядке убывания count.
 
Оптимальность обработки второго запроса учитывается при оценке тестовго задания. 
Покрытие кода тестами RSpec является плюсом.
Должна быть команда, которая наполняет базу данными из yml файла.
Используем последние версии Ruby, Rails и PSQL.
