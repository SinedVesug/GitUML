# GitUML
## Заказ и доставка еды из ресторана
classDiagram
class Ресторан{
 +String Название
 +String Адрес
 +String Телефон
 +String Сайт
}
class Меню{
 +String Блюдо
 +String Описание
 +Decimal Цена
}
class Клиент{
 +String Имя
 +String Телефон
 +String Адрес
}
class Заказ{
 +Int ID
 +Клиент Клиент
 +ПозицияЗаказа Блюдо
 +String Способ оплаты
 +String Статусы
 +DateTime Дата/Время
}
class ПозицияЗаказа{
 +Int ID
 +Меню Блюдо 
 +Int Количество
}
ПозицияЗаказа .. Меню
Заказ .. Клиент
Заказ ..> ПоизицияЗаказа
Ресторан <|-- Меню
Клиент <|-- Заказ
Заказ <|-- ПозицияЗаказа