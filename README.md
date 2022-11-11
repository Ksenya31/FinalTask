# Домашнее задание к занятию «4.2. Заключительная лекция»
**План автоматизации тестирования возможности записаться на обучение профессии «Тестировщик ПО»**
### 1.Перечень автоматизируемых сценариев.
***Поиск курса "Тестировщик ПО"***

1.1 Зайти на главную страницу [Нетология](https://netology.ru/#/)
+ Кликнуть на "Каталог курсов"
+ Кликнуть "Полный каталог"
+ Кликнуть "Тестировщик ПО"
+ Нажать на кнопку "Записаться"

1.2 Сценарий №2
+ Зайти на главную страницу [Нетология](https://netology.ru/#/)
+ Кликнуть на "Программирование"
+ Кликнуть "Тестировщик ПО"
+ Нажать на кнопку "Записаться"
	
1.3 Сценарий №3
+ Зайти на главную страницу [Нетология](https://netology.ru/#/)
+ Кликнуть на "355 курсов всех направлений"
+ Кликнуть "Тестировщик ПО"
+ Нажать на кнопку "Записаться"
	
1.4 Сценарий №4
+ Зайти на главную страницу [[Нетология](https://netology.ru/#/)
+ Кликнуть на "Обучение" (Footer сайта)
+ Кликнуть на "Программирование"
+ Кликнуть "Тестировщик ПО"
+ Нажать на кнопку "Записаться"
	
1.5 Сценарий №5
+ Зайти на главную страницу [[Нетология](https://netology.ru/#/)
+ Кликнуть на "Обучение" (Footer сайта)
+ Кликнуть на "Популярные курсы"
+ Кликнуть "Тестировщик ПО"
+ Нажать на кнопку "Записаться"
	
1.6 Сценарий №6
+ Зайти на главную страницу [[Нетология](https://netology.ru/#/)
+ Кликнуть на "Обучение" (Footer сайта)
+ Кликнуть на "Каталог курсов"
+ Кликнуть "Тестировщик ПО"
+ Нажать на кнопку "Записаться"
		
### Заполнение и отправка формы заявки
| Отправка                                               |Результат                             |
|--------------------------------------------------------|--------------------------------------|
|**Заполнение полей валидными данными** -> клик по кнопке "Записаться" | Данные успешно отправлены, появится всплывающее окно об успешном завершении записи|
|**Отправка пустой формы:** клик по кнопке "Записаться".|Данные не отправлены. Под каждым полем появилась надпись "Обязательное поле"|
|**Отправка формы с пустым полем "имя"** , заполнить поля "Номер телефона" и "Электроння почта" валидными данными -> клик по кнопке "Записаться"|Данные не отправлены. Под полем "Имя" появилась надпись "Обязательное поле"|	
|**Отправка формы с пустым полем "Номер телефона"** , заполнить поля "Имя" и "Электроння почта" валидными данными -> клик по кнопке "Записаться"|Данные не отправлены. Под полем "Номер телефона" появилась надпись "Обязательное поле"|
|**Отправка формы с пустым полем "Электронная почта"** , заполнить поля "Имя" и "Номер телефона" валидными данными -> клик по кнопке "Записаться"|Данные не отправлены. Под полем "Электронная почта" появилась надпись "Обязательное поле"|
|**Валидация каждого из полей на отображение соотвествующих ошибок:**||
|поле "Имя" заполняется цифрами и спецсимволами "1235№;;%", остальные поля заполняются валидными данными -> клик по кнопке "Записаться".|Данные не отправлены, под полем "Имя" появится сообщение "Должно состоять из букв".|
|поле "Имя" заполняется одним буквенным символом "а", остальные поля заполняются валидными данными -> клик по кнопке "Записаться"|Данные не отправлены, под полем "Имя" появится сообщение "Должно быть не короче 2 символов".|
|поле "Номер телефона" заполняется символами ";"№;№№", буквами "ваня", "DSDWFW"-> клик по кнопке "Записаться" |Данные не отправлены, под полем "Номер телефона" появится сообщение "Номер в формате +9 (999) 999-99-99"|
|поле "Электронная почта" заполняется без доменной части имени с точкой (.)., остальные поля заполняются валидными данными -> клик по кнопке "Записаться"|Данные не отправлены, под полем "Электронная почта" появится сообщение "Неверный email"|
|||
|**Отправка формы с данными из ранее успешно отправленой формы:** заполнение полей ранее успешно отправленными валидными данными -> клик по кнопке "Записаться" (из пункта успешная отправка).|Данные отправлены; появится всплывающее окно о ранее созданной записи.|
|||

## 2.Перечень используемых инструментов с обоснованием выбора.
**IntelliJ IDEA** - интегрированная среда разработки программного обеспечения, в которой будет выполняться написание автоматизированных сценариев;
**Java (JDK 11)** - объектно-ориентированный язык программирования, на котором будет выполняться написание автоматизированных сценариев;
**Gradle** - система автоматической сборки;
**JUnit5** - библиотека для тестирования программного обеспечения;
**Lombok** - библиотека генерации кода;
**Faker** - библиотека генерации данных, с помощью которой, будут созданы данные пользователя (клиента банка);
**Selenide** - инструмент для тестирования Web-приложений;
**AppVeyor** - веб-сервис непрерывной интеграции, предназначенный для сборки и тестирования;
**Allure** - инструмент построения отчетов автотестов
**Git, GitHub**- для хранения кода автотестов
## 3.Перечень необходимых разрешений, данных и доступов.
+ необходимо разрешение на проведение тестирования администрации веб-сайта Нетологии;
+ необходим доступ к базе данных записи на обучение профессии "Тестировщик ПО".

## 4.Перечень и описание возможных рисков при автоматизации.
+ большое количество автотестов тяжело поддерживать в актуаьном состоянии, модифицировать;
+ минимальное количество тестов — покрывают малую часть функциональности, большая вероятность пропустить баг или неисправность системы;
+ тесты могут быть плохо написанными, медленно запускаться, нет быстрой обратной связи, что может привести к тому что их вобще не будут запускать; 
+ тесты которые не поддерживают в актуальном состоянии, они вызывают ложные срабатывания, что ведет к отсутствию доверия к 
системе.

## 5.Перечень необходимых специалистов для автоматизации.
## 6.Интервальная оценка с учётом рисков в часах
