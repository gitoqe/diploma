plantuml.com/plantuml/uml/ZT0nJiD040NGFgUOsXsS80WQIo05AAY7zJTUOizQEsCG7L3GKd0HYme9vGwxDyAE4RHflvvczFzQZQCztkggeFIHljEOFjCkZVcTyaj-pSzJi4jV-IsDgwAWSnx4DMGDg8_X7iwcjA3JqFKj37Hjl4KJsWgHhg3Ww9gzACMRvvRA6NOGO_D1QDEop7VFeFvEg6zOiVSNeK9BeQOJBPKsCJYeGly-LPCwX1qTw8wNhs0T8XRL8zOXTYmErC6YTxfKgI3cwoUw7BpRqesNEV_Vm8k41pRyjbb3gcdV7m00

```uml
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

http://www.plantuml.com/plantuml/uml/fLLDRzim33rFlqBeXc4Ru0uOi4kH1VNIjScXdR40EVN2saoYrQ8CIMvNRFtle-puAqk3fiiX2KNoYO-ao5FdmVfIvyBTAYh0WfOMKm-qod4qki4rt2bZnsFvMxoofgHiOYoXbPy-YqVX2giyoZStYJKfEYT_WZq1cwwL1eyVRqgdY8-ZebQtzZ17UwTItBA7eiXL2buPYbnjqRbCZ2uC8VazJcbZ8qHBGXvDWJB-JNDG-aXAS78waQDH6_LuF23w-kicx3x610fVMfGpMXghgzjggCdiKAWhuzNouPhYB5C11t8vzt2BQvDdQDrHGBsAvuV2BY1N6IUaybySwZsZEtHUhHg0Wraby50v9izo55o13r5cxYdY3FObPjuN5trXO9W8mRcFh5gjVSJWmJ6ahJjPY4LFcec-TJBea7aAH8fM5GEt4GAHfb6tYSHTqmswf7JUQ7uTa6bIpjjDep1gkb75cLQTwYLtX3Pskswe5F-BdrX5_aNikGDqU9xFT1HjdgEoYCQX3Px8KSzW5yLQ6yg_HxtOfvo99lPQvkPeqz2uRnqC--VCf6NmlwPB85XX_N_-u3pggZPdbzLxxeROdW9V8CzNoAzfykDo0CBoFo1FeamvaVAjZE-1HqrYsAGQENts5UWqJk9dXpO0FLS4bAeGwIxSynsuMnqGid9S5iT_nksZwvyrAHU1-EPiTuk8YaLZigFGeWgdmQsBBKIEAwHCvhZqujilq0LpN5gZfLypsJYi65TQ9idB0nnAvykCfzoxxmNI1I_3ulsnc2EAB_mHlQadJvhD9vlDjp5f7uOyaRt59PjjrvXrITiox3OSXgKMuXUd_1Ks-5y0
```
@startuml
skinparam rectangle<<behavior>> {
	roundCorner 25
}

rectangle "СУБД\nSqlite" as DB
rectangle "Маршрутизация\nExpress.js" as EX
rectangle "Бизнес-логика\nNode.js" as Node
rectangle "Формирование\nотображения\nReact.js" as React
rectangle "Шаблоны\nстраниц" as Temp
rectangle "Настройки\nстилей\nCSS/SASS" as CSS

DB <--> Node

React <--> Node
React <--> EX

Temp --> React

CSS --> React
CSS --> Temp

@enduml
```