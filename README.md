﻿#Задача, которую нужно решить для приглашения на собеседование тренинга EPAM 
Условие задачи
Имеется набор емкостей, в которые заливают жидкости. В одну емкость можно залить только одну жидкость, т.е. смешивать жидкости запрещается. Емкость заполняется на 95% от максимального объема. 
Описание емкостей:
– стенки емкостей прямые или наклонные с одинаковым углом наклона во всех направлениях;
– у наклонных емкостей основание меньшей площади всегда находится внизу;
– в основании прямых емкостей могут быть следующие фигуры: квадрат, прямоугольник, равнобедренная трапеция, правильный шестиугольник, круг, овал (эллипс);
– в основании наклонных емкостей могут быть следующие фигуры: квадрат, равнобедренная трапеция, правильный шестиугольник, круг;
– высота у всех емкостей одинаковая.
Список имеющихся жидкостей (в скобках указана плотность, кг/м3): бензин (740), керосин (820), машинное масло (910).
Создать консольное приложение, в котором последовательно выполнить следующие задания:
– залить произвольным образом жидкости в набор емкостей (не менее 10);
– отсортировать емкости по убыванию массы залитой в них жидкости;
– вывести на консоль в табличном виде (можно без границ) набор емкостей (полный состав атрибутов) и их содержимого; 
– найти наименьшую массу бензина, залитого в емкость.
Требования:
– Использовать объектно-ориентированный подход для описания сущностей предметной области.
– Набор емкостей инициализировать в коде с помощью конструктора или метода. Как следствие, не использовать внешние источники данных: консоль (т.е. ввод с клавиатуры), файлы, СУБД и т.п.
– Инициализацию выполнить без датчика случайных чисел. Передавать в конструктор константные значения. Например, залить керосин в прямую емкость, в основании которой прямоугольник со сторонами 45 см и 30 см.
– Приложение должно быть консольным. Не использовать графический интерфейс! Таким образом, приложение ничего не должно вводить, а только выводить результаты на консоль.
Предпочтения по выбору:
– языка программирования: 1) **Java**; 2) C++; 3) другой ООП язык.
– реализации сортировки и поиска: 1) **интерфейс внешних библиотек**  (н-р, метод sort() подходящего класса); 2) собственный код. 

Формульный ликбез:
`mass = volume * density`

```
стенки емкостей  | 	volume = 
прямые           |	baseSquare * height
наклонные		 | (baseSquare1 + sqrt(baseSquare1 * baseSquare2) + baseSquare2) * height / 3
```

```
основание               | square = 
квадрат       			| a * a
прямоугольник 			| a * b
трапеция	  			| (a + b) * h / 2
правильный шестиугольник| a * a * sqrt(27) / 2
круг					| PI * a * a
овал (эллипс)			| PI * a * b