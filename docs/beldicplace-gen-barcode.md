# Массовое формирование штрих-кода

Процедура генерации штрих-кода для объектов раздела **Местонахождение инвентарных объектов**.

## Установка

Скомпилировать процедуру [p_beldicplace_gen_barcode](../src/p_beldicplace_gen_barcode.sql).

Добавить в Парус-Бюджет 8 пользовательскую процедуру:

|Мнемокод|Наименование|Тип|Способ выполнения|Имя хранимой процедуры|Блокировка при выполнении|Пиктограмма|
|---|---|---|---|---|---|---|
|BelObjPlaceBarcode|Сгенерировать штрих-код|Процедура|Ручной|P_BELDICPLACE_GEN_BARCODE|Нет|

Настроить параметры:

|Позиция|Наименование параметра|Тип данных|Тип параметра|Описание параметра|Визуализация|Привязка|Обязательный|Раздел|Метод вызова|Параметр|Родительский параметр|Дополнительный словарь|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|1|NCOMPANY|Число (number)|Входной (in)|NCOMPANY|Нет|К организации|Да||||||
|2|NIDENT|Число (number)|Входной (in)|NIDENT|Нет|К идентификатору отмеченных записей|Да||||||
|3|SUNITCODE|Строка (varchar2)|Входной (in)|SUNITCODE|Нет|К коду раздела|Да||||||

Настроить связь с разделом:

|Наименование раздела|Наименование привязки|Обновление после выполнения|Завершение транзакции|Подтверждение выполнения|Текст подтверждения|
|---|---|---|---|---|---|
|Местонахождение инвентарных объектов|Сгенерировать штрих-код|Текущую запись|Нет|Нет||