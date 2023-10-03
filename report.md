## Запрос всей таблицы 

![image](https://github.com/xisqzz/db_practice/assets/144116612/e38074e3-a7a5-418b-8304-8ce7510f8451) 

Выполняет запрос всей таблицы. * - означает все  

## Результат

![image](https://github.com/xisqzz/db_practice/assets/144116612/51e92fd6-234a-4150-95b1-eff92acd4a51)

## Запрос определенного столбца 

![image](https://github.com/xisqzz/db_practice/assets/144116612/ec72dcef-f939-4220-8ecb-19e2fcbc5805)

Выводит столбец id из таблицы качалка54

## Результат 

![image](https://github.com/xisqzz/db_practice/assets/144116612/41671f48-9b0a-4ca9-839a-cebd919b4cff)

## Запрос с условием 

![image](https://github.com/xisqzz/db_practice/assets/144116612/37b1be32-9735-466c-bee8-8e7af740b301)

Выводит все из таблицы абонимент где id = 2

## Результат 

![image](https://github.com/xisqzz/db_practice/assets/144116612/bd0e13f7-1048-4ff1-b250-784230b31e93)

## Сортировка 

![image](https://github.com/xisqzz/db_practice/assets/144116612/6e0d868b-6cde-4e77-b04e-9cc3a2f53b1a)

Выполняет сортировку таблицы качки по порядку чисел, где id больше 0

## Результат 

![image](https://github.com/xisqzz/db_practice/assets/144116612/a59fde62-dd9b-4390-b87a-be3672e46da5)


##Задание 13.09.2023

##Задание 1 

![image](https://github.com/xisqzz/db_practice/assets/144116612/c6294f5d-81c4-4fe7-9b0d-03a75eb48d7e)

Объединяет таблицу menu и person. Объединяет столбцы id и pizza_name

##Задание 2 

![image](https://github.com/xisqzz/db_practice/assets/144116612/96a40f7a-1a37-485b-9c73-2465caf4bad5)

Объединяет таблицу menu и person. Объединяет столбцы pizza_name и name

##Задание 3 

![image](https://github.com/xisqzz/db_practice/assets/144116612/50cb6a50-ff7c-46f6-bc92-cff07c419089)

Выбирает person_id из таблицы person_order, но только где order_date совпадает 
с датами посещений visit_date из таблицы person_visits. 

##Задания 19.09.2023

##Задание 1 

![image](https://github.com/xisqzz/db_practice/assets/144116612/849cf873-e597-4a2a-b6a1-adf1849332de)

Запрос создает комбинацию всех записей из таблицы person с каждой записью из таблицы pizzeria, а затем выбирает определенные столбцы из этой комбинации и сортирует результаты по person.id и pizzeria.id. Результат содержит все возможные сочетания между людьми и пиццериями из исходных таблиц.

##Задание 2 

![image](https://github.com/xisqzz/db_practice/assets/144116612/287890b9-0e8f-4ad3-b2b1-f8fa72488d58)

Выбирает данные о посещениях из таблицы person_visits и имена людей из таблицы person, соединяя их на основе соответствия person_id. 
Результаты сортируются по дате посещения в возрастающем порядке, а затем по именам людей.

##Задание 3 

![image](https://github.com/xisqzz/db_practice/assets/144116612/1d81f861-a670-49ad-b183-952c0dbc8723)

Запрос выбирает информацию о заказах из таблицы person_order и имя и возраст из таблицы person, соединяя их на основе соответствия person_id. Результаты сортируются сначала по дате заказа в возрастающем порядке, а затем по информации о человеке в алфавитном порядке.

##Задание 4 

![image](https://github.com/xisqzz/db_practice/assets/144116612/bbfc1c96-dde0-4349-b093-96a67798315a)



##Задание 5 

IN 

![image](https://github.com/xisqzz/db_practice/assets/144116612/9e3f4740-e7f9-45af-b091-ac8fb6468a75)

Запрос из таблицы pizzeria берет name и id, с условием pizzeria.id нету в person_visits. Выполняется с помощью IN

EXISTS

![image](https://github.com/xisqzz/db_practice/assets/144116612/18c42724-2b06-4495-a1c4-be80e1642d5c)

Запрос из таблицы pizzeria берет name и id, которые не имеют соотвествующих записей в таблице person_visits

##Задания 20.09.2023

##Задание 1 

![image](https://github.com/xisqzz/db_practice/assets/144116612/dcffc51e-d158-4e49-8ed9-d073ac3bd056)

Запроса содержит имена и рейтинги пиццерий из таблицы pizzeria, которые имеют рейтинг выше 3 и при этом не были посещены ни одним из клиентов.

##Задание 2 

![image](https://github.com/xisqzz/db_practice/assets/144116612/2f7ee40c-eb7c-49b4-8c82-6b57e7020c26)

Запрос содержит дату посещения и id человека (person_id) для посещений, в диапозоне между 1 января 2022 года и 10 января 2022 года и были посещены людьми с id 1 или 2

26.09.2023

Задание 1

![image](https://github.com/xisqzz/db_practice/assets/144116612/192dd18a-82e5-4586-8638-d3131d1410d8)

Выбирает все из таблицы students

Задание 2 

![image](https://github.com/xisqzz/db_practice/assets/144116612/e763743e-3929-4355-b44e-8e77e1dbe753)

Запрос берет из таблицы students имя, фамилию и возраст с условием что возраст больше 21  

Задание 3 

![image](https://github.com/xisqzz/db_practice/assets/144116612/1007c274-b6c0-464c-ae9f-15977c2fb1a0)

Выбирает все из таблицы studentcourses

Задание 4 

![image](https://github.com/xisqzz/db_practice/assets/144116612/59be8aff-8e65-49ea-84ae-5c7988c27e67)

Из таблицы students, studentcourses берутся имя, фамилия и id курса, с условием что courdeid = 1

Задание 5 

![image](https://github.com/xisqzz/db_practice/assets/144116612/a94b958b-b5d1-4aa8-b8e7-75ae5708095c)

Из таблиц students, studentcourses берутся имя, фамилия, возраст и id курса, с условием что courseid = 2 и age = 20

Задание 7

![image](https://github.com/xisqzz/db_practice/assets/144116612/430d4220-4250-48a9-b0cf-10d998777f20)

Вычисляет средний возраст студентов. Функция AVG вычисляет средний возраст из столбца age 

Задание 8 

![image](https://github.com/xisqzz/db_practice/assets/144116612/cafee5b4-ece3-49d1-bb2a-68fe035d5018)

Запрос содержит имена и фамилии студентов из таблицы students, которые не имеют записей в таблице studentcourses,
при условии что студенты не зарегистрированы ни на одном из курсов

Задание 10

![image](https://github.com/xisqzz/db_practice/assets/144116612/ddf7fdb8-2b33-4942-bc75-1aba785aca08)

Запрос берет имя, фамилию, возраст и id курса из таблиц students и studentcourses, с условием что courdeid = 3 age больше или равен 22

Задание 4

![image](https://github.com/xisqzz/db_practice/assets/144116612/3e1f0b77-46d7-4a6d-a703-e746e63ffee6)

Запрос берет из таблиц students, courses имя фамилию и id курса, при условии что courseid не равен 4

Задание 6 

![image](https://github.com/xisqzz/db_practice/assets/144116612/bbeb9d07-54a2-4e1c-85ed-69d86ef97804)

Запрос содержит имена, фамилии и возраст студента или студентов, 
чей возраст является наибольшим в таблице students.

Задание 8 

![image](https://github.com/xisqzz/db_practice/assets/144116612/a4cf130c-9655-4993-95c8-d182b9156067)

Задание 9 

![image](https://github.com/xisqzz/db_practice/assets/144116612/1e904e16-11f2-450a-89cc-851a78e406e2)

Из таблицы students берется его имя и фамилия. Результатом условия будут студенты старше 18 лет 
и которые не зарегистрированы ни на одном из курсов


