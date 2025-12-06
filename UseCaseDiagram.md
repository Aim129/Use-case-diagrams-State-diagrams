%% Diagram: Library Network Management System - Use Case Diagram

usecaseDiagram

actor Reader as R
actor Librarian as L
actor Administrator as A

R <|-- L
L <|-- A

usecase UC1 as "Регистрация пользователя"
usecase UC2 as "Просмотр книг"
usecase UC3 as "Поиск книг"
usecase UC4 as "Бронирование книги"
usecase UC5 as "Отмена бронирования"
usecase UC6 as "Просмотр истории бронирований"

usecase UC7 as "Управление книгами"
usecase UC7a as "Добавление книги"
usecase UC7b as "Удаление книги"

usecase UC8 as "Выдача книги"
usecase UC9 as "Возврат книги"

usecase UC10 as "Просмотр активных бронирований"

usecase UC11 as "Управление филиалами"
usecase UC12 as "Управление учетными записями"
usecase UC13 as "Просмотр аналитики"

UC7 --> UC7a : <<include>>
UC7 --> UC7b : <<include>>

%% Reader use cases
R --> UC1
R --> UC2
R --> UC3
R --> UC4
R --> UC5
R --> UC6

%% Librarian use cases
L --> UC7
L --> UC8
L --> UC9
L --> UC10

%% Administrator use cases
A --> UC11
A --> UC12
A --> UC13
