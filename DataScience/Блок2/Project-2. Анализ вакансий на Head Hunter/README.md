# Проект 2. Анализ вакансий из Head Hunter

## Оглавление  
[1. Описание проекта](https://github.com/PavelALA/Project_1/blob/master/DataScience/Блок2/Project-2.%20Анализ%20вакансий%20на%20Head%20Hunter/README.md#Описание-проекта)  
[2. Какой кейс решаем?](https://github.com/PavelALA/Project_1/blob/master/DataScience/Блок2/Project-2.%20Анализ%20вакансий%20на%20Head%20Hunter/README.md#Какой-кейс-решаем)  
[3. Краткая информация о данных](https://github.com/PavelALA/Project_1/blob/master/DataScience/Блок2/Project-2.%20Анализ%20вакансий%20на%20Head%20Hunter/README.md#Краткая-информация-о-данных)  
[4. Этапы работы над проектом](https://github.com/PavelALA/Project_1/blob/master/DataScience/Блок2/Project-2.%20Анализ%20вакансий%20на%20Head%20Hunter/README.md#Этапы-работы-над-проектом)  
[5. Результат](https://github.com/PavelALA/Project_1/blob/master/DataScience/Блок2/Project-2.%20Анализ%20вакансий%20на%20Head%20Hunter/README.md#Результаты)    
[6. Выводы](https://github.com/PavelALA/Project_1/blob/master/DataScience/Блок2/Project-2.%20Анализ%20вакансий%20на%20Head%20Hunter/README.md#Выводы) 

### Описание проекта    
Проект по составлению SQL-запросов и анализу полученных результатов.

:arrow_up:[к оглавлению](https://github.com/PavelALA/Project_1/blob/master/DataScience/Блок2/Project-2.%20Анализ%20вакансий%20на%20Head%20Hunter/README.md#Оглавление)


### Какой кейс решаем?    
Кадровое агентство подбирает вакансии для IT-специалистов. Первый проект — создание модели машинного обучения, которая будет рекомендовать вакансии клиентам агентства, претендующим на позицию Data Scientist. Сначала необходимо понять, что из себя представляют данные и насколько они соответствуют целям проекта. В литературе эта часть работы над ML-проектом называется Data Understanding, или анализ данных.


### Краткая информация о данных
Ознакомимся с представленными в таблицах данными

1. ***VACANCIES*** - Таблица хранит в себе данные по вакансиям и содержит следующие столбцы:
    - **id** - int4 - ID вакансии;
    - **name** - text -  Название вакансии;
    - **key_skills** - text - Ключевые навыки;
    - **schedule** - text - Тип рабочего графика;
    - **experience** - text - Требования к опыту;
    - **employment** - text - Тип трудоустройства;
    - **salary_from** - int4 - Нижняя граница зарплатной вилки;
    - **salary_to** - int4 - Верняя граница зарплатной вилки;
    - **area_id** - int4 - ID региона вакансии;
    - **employer_id** - int4 - ID работодателя;

2. ***AREAS*** - Таблица-справочник, которая хранит код города и его название:
    - **id** - int4 - Идентификатор города;
    - **name** - text - Название города;

3. ***EMPLOYERS*** - Таблица-справочник со списком работодателей:
    - **id** - int4 - Номер работодателя;
    - **name** - text - Название работодателя;
    - **area** - int4 - Регион регистрации;

4. ***INDUSTRIES*** - Таблица-справочник вариантов сфер деятельности работодателей:
    - **id** - varchar(10) - ID сферы деятельности;
    - **name** - text - Название сферы деятельности:

5. ***EMPLOYERS_INDUSTRIES*** - Дополнительная таблица, которая существует для организации связи между работодателями и сферами их деятельности:
    - **employer_id** - int4 - ID работодателя:
    - **industry_id** - archar(10) - ID сферы деятельности;
  
:arrow_up:[к оглавлению](https://github.com/PavelALA/Project_1/blob/master/DataScience/Блок2/Project-2.%20Анализ%20вакансий%20на%20Head%20Hunter/README.md#Оглавление)


### Этапы работы над проектом  
1. __Прндваритеьный анализ данных__: на данном этапе производим ознакомление и основной подсчет значений, хранящихся в таблицах.
2. __Детальный анализ вакансий__: ознакомление и анализ данных предсталенных в датасете касаемо вакансий, поиск аномаьных данных.
3. __Анализ работодателй__: ознакомление и анализ данных предлставленных а датасете о работодателях: численность вакасий, задействованность в регионах, указание сфер деятельности.
4. __Предметный анализ__: анализ вакансий и работодателей на востребованность специализации DataScientist, количество таких вакансий, рапределение по уровням знаний, опыта и оплаты труда, выявление основных требований к данной специальности, определение наиблее востребованного рабочего времени и типа трудоустройства.

:arrow_up:[к оглавлению](https://github.com/PavelALA/Project_1/blob/master/DataScience/Блок2/Project-2.%20Анализ%20вакансий%20на%20Head%20Hunter/README.md#Оглавление)


### Результаты:  
В результате выполненной работы мы получили анлиз по каждому этапу и обощенный анализ, в которых выявляем осноыне связи данных, дальнейшее направление исследования а также возможные ошибки в данных, которые могут повлиять на дальнейшее моделирование. 

:arrow_up:[к оглавлению](https://github.com/PavelALA/Project_1/blob/master/DataScience/Блок2/Project-2.%20Анализ%20вакансий%20на%20Head%20Hunter/README.md#Оглавление)


### Выводы:  
По результатам нализа данных получаем направление дальнешей работы по исследованию данных.

:arrow_up:[к оглавлению](https://github.com/PavelALA/Project_1/blob/master/DataScience/Блок2/Project-2.%20Анализ%20вакансий%20на%20Head%20Hunter/README.md#Оглавление)
