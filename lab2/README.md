# Лабораторная работа #2
<ins>Задание.</ins>

По варианту, выданному преподавателем, составить и выполнить запросы к [базе данных "Учебный процесс"](https://github.com/CandyGoose/ITMO_Software_engineering/tree/main/2_term_Software_engineering/Database/lab2/БД_Учебный_Процесс.pdf).

Команда для подключения к базе данных ucheb:

_psql -h pg -d ucheb_

<ins>Отчёт по лабораторной работе должен содержать:</ins>
1. Текст задания.
2. Реализацию запросов на SQL.
3. Выводы по работе.

<ins>Темы для подготовки к защите лабораторной работы:</ins>
1. SQL
2. Соединение таблиц
3. Подзапросы

### Номер варианта: _3_
## Внимание! У разных вариантов разный текст задания!
Составить запросы на языке SQL (пункты 1-7).
1. Сделать запрос для получения атрибутов из указанных таблиц, применив фильтры по указанным условиям:
    
    Таблицы: Н_ЛЮДИ, Н_ВЕДОМОСТИ.
    
    Вывести атрибуты: Н_ЛЮДИ.ИМЯ, Н_ВЕДОМОСТИ.ИД.

    Фильтры (AND):

    a) Н_ЛЮДИ.ФАМИЛИЯ < Иванов.

    b) Н_ВЕДОМОСТИ.ИД = 1250981.

    c) Н_ВЕДОМОСТИ.ИД = 1250972.

    Вид соединения: RIGHT JOIN.

2. Сделать запрос для получения атрибутов из указанных таблиц, применив фильтры по указанным условиям:

    Таблицы: Н_ЛЮДИ, Н_ВЕДОМОСТИ, Н_СЕССИЯ.

    Вывести атрибуты: Н_ЛЮДИ.ОТЧЕСТВО, Н_ВЕДОМОСТИ.ДАТА, Н_СЕССИЯ.ИД.

    Фильтры (AND):

    a) Н_ЛЮДИ.ИД < 100012.

    b) Н_ВЕДОМОСТИ.ИД = 1457443.

    Вид соединения: RIGHT JOIN.

3. Вывести число студентов ФКТИУ, которые старше 25 лет.

    Ответ должен содержать только одно число.

4. В таблице Н_ГРУППЫ_ПЛАНОВ найти номера планов, по которым обучается (обучалось) более 2 групп на заочной форме обучения.

    Для реализации использовать соединение таблиц.

5. Выведите таблицу со средними оценками студентов группы 4100 (Номер, ФИО, Ср_оценка), у которых средняя оценка меньше минимальной оценк(е|и) в группе 3100. 

6. Получить список студентов, отчисленных до первого сентября 2012 года с очной формы обучения (специальность: 230101). В результат включить:

    номер группы;

    номер, фамилию, имя и отчество студента;

    номер пункта приказа;

    Для реализации использовать соединение таблиц.

7. Вывести список людей, не являющихся или не являвшихся студентами СПбГУ ИТМО (данные, о которых отсутствуют в таблице Н_УЧЕНИКИ). В запросе нельзя использовать DISTINCT.