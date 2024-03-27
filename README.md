# Алгоритмы и структуры данных (ADS-5)

![GitHub pull requests](https://img.shields.io/github/issues-pr/NNTU-CS/ADS-5)
![GitHub closed pull requests](https://img.shields.io/github/issues-pr-closed/NNTU-CS/ADS-5)

Срок выполнения задания:

**по 14 апреля** ![Relative date](https://img.shields.io/date/1713128400) 


## Задание

> Написать реализацию алгоритмов перевода арифметического выражения из инфиксной формы в постфиксную и вычисления выражения, записанного в постфиксной форме.

## Пояснение

В теме **Стек на массиве** приводится описание алгоритмов перевода арифметического выражения, заданного в виде строки из инфиксной формы в префиксную, то есть например:

`(2+2)*(3-1)` преобразуется в `2 2 + 3 1 - *`

Предполагается:

- входная строка содержит правильно построенное выражение
- числа положительные, целые, могут состоять из нескольких цифр
- все действия производятся над целыми, результат - целый

Для перевода из одной формы в другую мы используем стек, построенный на основе шаблона. Этот стек должен быть описан в файле **include/tstack.h**.

Для использования стека достаточно его инстанцировать с указанием типа данных:

```C++
TStack<char, 100> stack1;
TStack<int, 100> stack2;
```

Функции должны иметь следующую сигнатуру и располагаться в файле **src/alg.cpp**:


```C++
// преобразование выражение в постфиксную форму
std::string infx2pstfx(std::string inf) {

}
// вычисление выражения, записанного в постфиксной форме
int eval(std::string post) {

}

```
Описания параметров функций:

- **inf** - строка, содержащая запись арифметического выражения в инфиксной форме, например "(2+2)*2"
- **post** - строка, содержащая запись арифметического выражения в постфиксной форме, например "2 2 + 2 *"

В этом задании в качестве строк используется тип **std::string** из стандартной библиотеки С++

Описания функций:

- Функция **infx2pstfx** должна преобразовывать входную строку, содержащую выражение в инфиксной форме в выходную строку, которая содержит то же выражение в постфиксной фоме. Для отделения операндов друг от друга нужно использовать пробелы.

- Функция **eval** должна вычислять выражение, записанное в постфиксном виде и выдавать целое значение. Все расчеты ведутся в целых числах!

Помимо указанных функций, в файл **alg.cpp** можно помещать определения вспомогательных функций.
