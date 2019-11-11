# Модуль модификации управляемы форм

Предназначен для доработки типовых конфигураций для ускоренной программной модификации форм.

## Начало работы

Все вызовы модуля должны производиться из модуля формы при выполнении процедур ПриСозданииНаСервере и ПриЧтенииНаСервер.

## Предварительные требования

Модуль распространяется поставкой. 
Зависимостей не имеет.

### Установка

Уставновка производится через сравнение/объединения конфигурации с файлом поставки, с установкой на поддержку.

## Использование

Вариант 1
``` bsl
КонтекстФормы = РедакторФорм.СоздатьКонтекстЭлемента(ЭтотОбъект);	
КонтекстФормы.Свойства.Вставить("Вид", ВидГруппыФормы.ОбычнаяГруппа);
КонтекстФормы.Свойства.Вставить("Группировка", ГруппировкаПодчиненныхЭлементовФормы.ГоризонтальнаяЕслиВозможно);
КонтекстФормы.Свойства.Вставить("ОтображатьЗаголовок", Ложь);
ЭлементГруппаШапка = РедакторФорм.ДобавитьГруппуНаФорму(КонтекстФормы, "ГруппаШапка"); 
```
Вариант 2
``` bsl
Свойства = Новый Структура("Вид, ОтображатьЗаголовок", ВидГруппыФормы.ОбычнаяГруппа, Ложь);
КонтекстФормы = РедакторФорм.СоздатьКонтекстЭлемента(ЭтотОбъект, , ,Свойства);	
ЭлементГруппаШапка = РедакторФорм.ДобавитьГруппуНаФорму(КонтекстФормы, "ГруппаШапка"); 
```
## Запуск тестов

Тесты запускаются через vanessa runner: файл run_vanessa.bat.

## Authors

See the list of [contributors](https://github.com/huxuxuya/FormModificator/contributors) who participated in this project.

