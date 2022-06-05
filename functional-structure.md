## План наполнения страниц v.1

```plantuml
@startwbs
* Главная страница Учебного центра
** Сведения об организации
*** Документы
*** Структура и органы управления
*** Материально-техническое обеспечение
*** Образовательные стандарты
*** Независимая оценка качества
*** Противодействие коррупции
*** Инклюзивное образрваеие
** Обучение
*** Расписание занятий групп
*** График учебных недель
*** О Компьютерной школе
**** Информация о курсах для дошкольников
**** Информация о курсах для начальной школы
**** Информация о базовых курсах
**** Информация о профильных курсах
**** Информация о курсах программирования
** Аренда
@endwbs
```

## Схема функциональных компонентов приложения

```plantuml
@startuml
skinparam rectangle<<behavior>> {
	roundCorner 25
}

rectangle "Sqlite\n\nСУБД" as DB
rectangle "Express.js + Node.js\n\nAPI, серверная\nчасть" as EX
rectangle "Angular\n\nКлиентская\nчасть" as Angular
rectangle "Angular\n\nШаблоны\nHTML" as Temp
rectangle "CSS/SASS\n\nНастройки\nстилей" as CSS

rectangle "Bulma\n\nCSS-библиотека" as Bulma

Bulma --> CSS
EX <--> DB
EX <--> Angular
Temp <--> Angular
CSS --> Angular
CSS --> Temp
@enduml
```

## Структурная схема проектируемого веб-ресурса

```plantuml
@startwbs
* Главная страница
** Поступление
** Курсы
***: Страницы
отдельных
курсов;
** Расписание
** Работы учеников
** Об организации
***: Сведения
об организации;
*** Документы
*** Сотрудники
** Оплата и аренда
*** Оплата
*** Аренда
@endwbs
```
## OLD ONE
### Главная
```plantuml
@startwbs
* Главная
** Мезон
**:Сведения
об
организации;
**:Обучение
(неактуально);
** Аренда
** Расписание
**:Стоимость
(неактуально);
** Итоговые работы
**:Полезные ссылки
(неактуально);
**:Мероприятия
(неактуально);
@endwbs
```
### Сведения об организации
```plantuml
@startwbs
* Сведения об организации
**:Основные
сведения;
** Документы
** Образование
**:Образовательные
стандарты;
**:Руководство
и педагогический
состав;
**:Структура
и органы управления;
**:Материально-техническое
обеспечение и оснащенность
образовательного процесса;
**:Стипендии
и иные виды
материальной
поддержки;
**:Платные
образовательные
услуги;
**:Финансово и 
хозяйственная
деятельность;
**:Вакантные места
для приема/перевода;
@endwbs
```


```plantuml
@startwbs
* Главная страница
** Главная




** Обучение
** Аренда

***: Страницы
отдельных
курсов;
** Расписание
** Работы учеников
** Об организации
***: Сведения
об организации;
*** Документы
*** Сотрудники
** Оплата и аренда
*** Оплата
*** Аренда
@endwbs
```

## Диаграмма объектов БД

```plantuml
@startuml
' hide the spot
hide circle

' avoid problems with angled crows feet
skinparam linetype ortho

entity "Courses" as Courses {
  *id : INTEGER <<generated>>
  --
  - name : TEXT
  - description : TEXT
  - subscription : TEXT
  - price : TEXT  
  - next_course: INTEGER id <<FK>>
  - level : TEXT name <<FK>>
  - grade : INTEGER
  - themes : BLOB
  - time : INTEGER
}

entity "Levels" as Levels {
  *id : INTEGER <<generated>>
  --
  - name : TEXT
}

Levels --> Courses

entity "Students_work" as Students_work {
  *id : INTEGER <<generated>>
  --
  - course_id : INTEGER <<FK>>
  - year : TEXT
  - student_name : TEXT
  - link : TEXT
}

Courses --> Students_work

entity "Employees" as Employees {
  *id : INTEGER <<generated>>
  --
  - name : TEXT
  - surname : TEXT
  - middlename : TEXT
  - position : TEXT
  - education : TEXT
  - start_year : TEXT
  - experience : TEXT
}

entity "Teaches" as Teaches {
  *id : INTEGER <<generated>>
  --
  - course_id : INTEGER <<FK>>
  - teacher_id : INTEGER <<FK>>
}

Courses --> Teaches
Employees --> Teaches

@enduml
```



































