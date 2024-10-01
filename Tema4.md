# Тема 4. Функции и стандартные модули/библиотеки.
Отчет по Теме #4 выполнила:
- Курбатова Анна Сергеевна
- ИВТ-22-2

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 | + |   |
| Задание 7 | + |   |
| Задание 8 | + |   |
| Задание 9 | + |   |
| Задание 10 | + |   |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №4
## Задание 1.
### Напишите функцию, которая выполняет любые арифметические действия и выводит результат в консоль. Вызовите функцию используя “точку входа”.
```python
def main():
    print(2+2)

if __name__ == '__main__':
    main()
```
### Результат.
![Задание1](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/z1.jpg)
## Выводы
1. `def main():`: Объявляем функцию main().
2. `print(2+2)`: Выводится cумма 2 и 2. Это число.
3. `if __name__ == '__main__':`: Точка входа в программу. Выполняется только при запуске самого модуля.
4. `main()`: Вызывается функция main().

## Задание 2.
### Напишите функцию, которая выполняет любые арифметические действия, возвращает при помощи return значение в место, откуда вызывали функцию. Выведите результат в консоль. Вызовите функцию используя “точку входа”.
```python
def main():
    return 2+2

if __name__ == '__main__':
    print(main())
```
### Результат.
![Задание2](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/z2.jpg)
## Выводы
1. `def main():`: Объявляем функцию main().
2. `return 2+2`: Возвращается cумма 2 и 2. Это число.
3. `if __name__ == '__main__':`: Точка входа в программу. Выполняется только при запуске самого модуля.
4. `print(main())`: Вызывается функция main() и выводится значение, которое возвращает функция.

## Задание 3.
### Напишите функцию, в которую передаются два аргумента, над ними производится арифметическое действие, результат возвращается туда, откуда эту функцию вызывали. Выведите результат в консоль. Вызовите функцию в любом небольшом цикле. На скриншоте ниже приведен пример программы, в которой аргумент функции “x“превращается в параметр “one”, то же самое происходит с “y” и “two”
```python
def main(one, two):
    result = one + two
    return result

for i in range(5):
    x = 1
    y = 10
    answer = main(x, y)
    print(answer)
```
### Результат.
![Задание3](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/z3.jpg)
## Выводы
1. `def main(one, two):`: Объявляем функцию main().
2. `result = one + two`: Объявляется и присваивается значение переменной result.
3. `return 2+2`: Возвращается значение переменной.
4. `for i in range(5):`: Цикл. i изменяется от 0 до 5.
5. `x = 1`: Объявляется и присваивается значение переменной.
6. `y = 10`: Объявляется и присваивается значение переменной.
7. `answer = main(x, y)`: Объявляется и присваивается значение переменной. 
8. `print(answer)`: Выводится переменная answer. Вызывается функция main с параметрами x и y.

## Задание 4.
### Напишите функцию, на вход которой подается какое-то изначальное неизвестное количество аргументов, над которыми будет производится арифметические действия. Для выполнения задания необходимо использовать кортеж “*args”. На скриншоте ниже приведен пример такой программы с комментариями. Для закрепления понимания работы с кортежами настоятельно рекомендуем поменять аргументы вызова функции, вручную посчитать результат, только потом запустить программу с новыми значениями и проверить себя, насколько вы поняли данный аспект программирования.
```python
def main(x, *args):
    one = x
    two = sum(args)
    three = float(len(args))
    print(f'one={one}\ntwo={two}\nthree={three}')

    return x + sum(args) / float(len(args))

if __name__ == '__main__':
    result = main(10, 0, 1, 2, -1, 0, -1, 1, 2)
    print(f'\nresult={result}')
```
### Результат.
![Задание4](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/z4.jpg)
## Выводы
1. `def main(x, *args):`:Объявляем функцию main().
2. `one = x`: Объявляется и присваивается значение переменной. 
3. `two = sum(args)`: Объявляется и присваивается значение переменной, функция sum() суммирует все элементы кортежа.
4. `three = float(len(args))`: Объявляется и присваивается значение переменной, функции len() возвращает длинну кортежа, float() возвращает число с плавающей точкой.
5. `print(f'one={one}\ntwo={two}\nthree={three}')`: Вывод на экран.
6. `return x + sum(args) / float(len(args))`: Возвращается значение математической операции.
7. `if __name__ == '__main__':`: Точка входа в программу. Выполняется только при запуске самого модуля.
8. `result = main(10, 0, 1, 2, -1, 0, -1, 1, 2)`: Объявляется и присваивается значение переменной.
9. `print(f'\nresult={result}')`: Вывод на экран. Вызов функции main().

## Задание 5.
### Напишите функцию, которая на вход получает кортеж “**kwargs” и при помощи цикла выводит значения, поступившие в функцию. На скриншоте ниже указаны два варианта вызова функции с “**kwargs” и два варианта работы с данными, поступившими в эту функцию. Комментарии в коде и теоретическая часть помогут вам разобраться в этом нелегком аспекте. Вызовите функцию используя “точку входа”.
```python
def main(**kwargs):
    for i in kwargs.items():
        print(i[0], i[1])

    print()

    for key in kwargs:
        print(f'{key} = {kwargs[key]}')

if __name__ == '__main__':
    main(x=[1,2,3], y=[3,3,0], z=[2,3,0], q=[3,3,0], w=[3,3,0])
    print()

    main(**{'x':[1,2,3], 'y':[3,3,0]})
```
### Результат.
![Задание5](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/z5.jpg)
## Выводы
1. `def main(**kwargs)::`:Объявляем функцию main().
2. `for i in kwargs.items():`: Цикл. Проходит по каждому элементу кортежа.  
3. `print(i[0], i[1])`: Вывод на экран.
4. `print()`: Вывод на экран.
5. `for key in kwargs:`: Цикл. Проходит по кажому ключу кортежа.
6. `print(f'{key} = {kwargs[key]}')`: Вывод на экран.
7. `if __name__ == '__main__':`: Точка входа в программу. Выполняется только при запуске самого модуля.
8. `main(x=[1,2,3], y=[3,3,0], z=[2,3,0], q=[3,3,0], w=[3,3,0])`: Вызов функции main() c параметрами.
9. `print()`: Вывод на экран.
10. `main(**{'x':[1,2,3], 'y':[3,3,0]})`: Вызов функции main() c параметрами.

## Задание 6.
### Напишите две функции. Первая – получает в виде параметра “**kwargs”. Вторая считает среднее арифметическое из значений первой функции. Вызовите первую функцию используя “точку входа” и минимум 4 аргумента.
```python
def main(**kwargs):
    for i, j in kwargs.items():
        print(f'{i}. Mean = {mean(j)}')

def mean(data):
    return sum(data) / float(len(data))

if __name__ == '__main__':
    main(x=[1,2,3], y=[3,3,0])
```
### Результат.
![Задание6](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/z6.jpg)
## Выводы
1. `def main(**kwargs):`:Объявляем функцию main().
2. `for i, j in kwargs.items():`: Цикл. Проходит по каждому элементу кортежа.  
3. `print(f'{i}. Mean = {mean(j)}')`: Вывод на экран.
4. `def mean(data):`: Объявляем функцию mean().
5. `return sum(data) / float(len(data))`: Возвращается значение математической операции.
6. `if __name__ == '__main__':`: Точка входа в программу. Выполняется только при запуске самого модуля.
7. `main(x=[1,2,3], y=[3,3,0])`: Вызов функции main() c параметрами.

## Задание 7.
### Создайте дополнительный файл .py. Напишите в нем любую функцию, которая будет что угодно выводить в консоль, но не вызывайте ее в нем. Откройте файл main.py, импортируйте в него функцию из нового файла и при помощи “точки входа” вызовите эту функцию.
main:
```python
from sup import say_hello

if __name__ == '__main__':
    say_hello()
```
sup:
```python
def say_hello():
    print('Hello students!')
```
### Результат.
![Задание7](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/z7.jpg)
## Выводы
1. `from sup import say_hello`: Импортируется функция say_hello().
2. `if __name__ == '__main__':`: Точка входа в программу. Выполняется только при запуске самого модуля.
3. `say_hello()`: Вызов функции say_hello().
4. `def say_hello():`: Объявляется функция say_hello().
5. `print('Hello students!')`: Вывод на экран строку 'Hello students!'.

## Задание 8.
### Напишите программу, которая будет выводить корень, синус, косинус полученного от пользователя числа.
```python
import math

def main():
    value = int(input('Введите значение: '))
    print(math.sqrt(value))
    print(math.sin(value))
    print(math.cos(value))

if __name__ == '__main__':
    main()
```
### Результат.
![Задание8](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/z8.jpg)
## Выводы
1. `import math`: Импортируется функции библиотеки math.
2. `def main():`: Объявляется функция main().
3. `value = int(input('Введите значение: '))`: Объявляется и присваивается значение переменной, введенное с клавиатуры.
4. `print(math.sqrt(value))`: Выводится значение функции sqrt() библиотеки math. Квадратный корень.
5. `print(math.sin(value))`: Выводится значение функции sin() библиотеки math. Синус числа.
6. `print(math.cos(value))`: Выводится значение функции cos() библиотеки math. Косинус числа.
7. `if __name__ == '__main__':`: Точка входа в программу. Выполняется только при запуске самого модуля.
8. `main()`: Вызов функции main().

## Задание 9.
### Напишите программу, которая будет рассчитывать какой день недели будет через n-нное количество дней, которые укажет пользователь.
```python
from datetime import datetime as dt
from datetime import timedelta as td

def main():
    print(
        f'Сегодня {dt.today().date()}. '
        f'День недели - {dt.today().isoweekday()}'
    )
    n = int(input('Введите количество дней: '))
    today = dt.today()
    result = today + td(days=n)
    print(
        f'Через {n} дней будет {result.date()} '
        f'День недели - {result.isoweekday()}'
    )

if __name__ == '__main__':
    main()
```
### Результат.
![Задание9](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/z9.jpg)
## Выводы
1. `from datetime import datetime as dt`: Импортируется функция библиотеки datetime. dt равно datetime.
2. `from datetime import timedelta as td`: Импортируется функция библиотеки datetime. td равно timedelta.
3. `def main():`: Объявляется функция main().
4. `print(
        f'Сегодня {dt.today().date()}. '
        f'День недели - {dt.today().isoweekday()}'
    )`: Выводится на экран сегодняшняя дата в формате ГГГГ-ММ-ДД, и текущий день недели 1 = понедельник, 2 = вторник, 3 = среда и так далее.
5. `n = int(input('Введите количество дней: '))`: Объявляется и присваивается значение переменной, введенное с клавиатуры.
6. `today = dt.today()`: Объявляется и присваивается значение переменной.
7. `result = today + td(days=n)`: Объявляется и присваивается значение переменной.
8. `print(
        f'Через {n} дней будет {result.date()} '
        f'День недели - {result.isoweekday()}'
    )`: Выводится на экран, какой день будет через n дней в формате ГГГГ-ММ-ДД и день недели 1 = понедельник, 2 = вторник, 3 = среда и так далее.
9. `if __name__ == '__main__':`: Точка входа в программу. Выполняется только при запуске самого модуля.
10. `main()`: Вызов функции main().

## Задание 10.
### Напишите программу с использованием глобальных переменных, которая будет считать площадь треугольника или прямоугольника в зависимости от того, что выберет пользователь. Получение всей необходимой информации реализовать через input(), а подсчет площадей выполнить при помощи функций. Результатом программы будет число, равное площади, необходимой фигуры.
```python
global result

def rectangle():
    a = float(input('Ширина: '))
    b = float(input('Длина: '))
    global result
    result = a * b

def triangle():
    a = float(input('Основание: '))
    h = float(input('Высота: '))
    global result
    result = 0,5 * a * h

figure = input('1-прямоугольник, 2-треугольник: ')
if figure == '1':
    rectangle()
elif figure == '2':
    triangle()

print(f'Площадь: {result}')
```
### Результат.
![Задание10](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/z10.jpg)
## Выводы
1. `global result`:  Объявляется глобальная переменная.
2. `def rectangle():`: Объявляется функция rectangle().
3. `a = float(input('Ширина: '))`: Объявляется и присваивается значение переменной, введенное с клавиатуры.
4. `b = float(input('Длина: '))`: Объявляется и присваивается значение переменной, введенное с клавиатуры.
5. `global result
    result = a * b`: Записывается значение произведения в глобальную переменную result.
6. `def triangle():`: Объявляется функция triangle().
7. `a = float(input('Основание: '))`: Объявляется и присваивается значение переменной, введенное с клавиатуры.
8. `h = float(input('Высота: '))`: Объявляется и присваивается значение переменной, введенное с клавиатуры.
9. `global result
    result = a * b`: Записывается значение произведения в глобальную переменную result.
10. `figure = input('1-прямоугольник, 2-треугольник: ')`: Объявляется и присваивается значение переменной, введенное с клавиатуры.
11. `if figure == '1':
    rectangle()
elif figure == '2':
    triangle()`: Условие. Если figure = 1, то выполняется функция rectangle(), если figure = 2, то выполняется triangle().
12. `print(f'Площадь: {result}')`: Вывод на экран.



## Самостоятельная работа №4
## Задание 1.
### Дайте подробный комментарий для кода, написанного ниже. Комментарий нужен для каждой строчки кода, нужно описать что она делает. Не забудьте, что функции комментируются по-особенному.
```python
from datetime import datetime 
from math import sqrt 
def main(**kwargs): 
    for key in kwargs.items(): 
        result = sqrt(key[1][0] ** 2 + key[1][1] ** 2) 
        print(result) 

if __name__ == '__main__': 
    start_time = datetime.now() 
    main( 
        one=[10, 3],
        two=[5, 4], 
        three=[15, 13], 
        four=[93, 53], 
        five=[133, 15] 
    ) 
    time_costs = datetime.now() - start_time 
    print(f"Время выполнения программы - {time_costs}")
```
### Результат.
![Задание1с](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/s1.jpg)
## Выводы
1. `from datetime import datetime`: Импортируется функция datetime() библиотеки datetime.
2. `from math import sqrt`: Импортируется функция sqrt() библиотеки math.
3. `def main(**kwargs): `: Объявляется функция main(), которая принимает параметр кортеж.
4. `for key in kwargs.items():`: Цикл. Проходит по каждому ключу кортежа.
5. `result = sqrt(key[1][0] ** 2 + key[1][1] ** 2) `: Объявляется и присваивается значение переменной.
6. `print(result)`: Выводится значение переменной result.
7. `if __name__ == '__main__':`: Точка входа в программу. Выполняется только при запуске самого модуля.
8. `start_time = datetime.now() `: Объявляется и присваивается значение переменной.
9. `main( 
        one=[10, 3],
        two=[5, 4], 
        three=[15, 13], 
        four=[93, 53], 
        five=[133, 15] 
    )`: Вызов функции main() c параметром кортеж.
10. `time_costs = datetime.now() - start_time`: Объявляется и присваивается значение переменной.
11. `print(f"Время выполнения программы - {time_costs}")`: Выводится "Время выполнения программы -" и значение переменной time_costs.

## Задание 2.
### Напишите программу, которая будет заменять игральную кость с 6 гранями. Если значение равно 5 или 6, то в консоль выводится «Вы победили», если значения 3 или 4, то вы рекурсивно должны вызвать эту же функцию, если значение 1 или 2, то в консоль выводится «Вы проиграли». При этом каждый вызов функции необходимо выводить в консоль значение “кубика”. Для выполнения задания необходимо использовать стандартную библиотеку random. Программу нужно написать, используя одну функцию и “точку входа”.
```python
import random

def main():
    cube = [1, 2, 3, 4, 5, 6]
    rand = random.choice(cube)
    print(f'Выпало {rand}')
    if rand == 5 or rand == 6:
        print('Вы победили!')
    elif rand == 3 or rand == 4:
        main()
    else:
        print('Вы проиграли!')


if __name__ == '__main__':
    main()
```
### Результат.
![Задание2с](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/s2.jpg)
## Выводы
1. `import random`: Импортируется функция random стандартной библиотеки.
2. `def main():`: Объявляется функция main().
3. `cube = [1, 2, 3, 4, 5, 6]`: Объявляется и присваивается значение переменной. 
4. `rand = random.choice(cube)`: Объявляется и присваивается значение переменной. 
5. `if rand == 5 or rand == 6:
        print('Вы победили!')
    elif rand == 3 or rand == 4:
        main()
    else:
        print('Вы проиграли!')`: Условие. Если выпало 5 или 6, то выводится 'Вы победили!'. Если выпало 3 или 4, то программа запускается снова. Если выпало 1 или 2, то выводится 'Вы проиграли!'.
6. `if __name__ == '__main__':`: Точка входа в программу. Выполняется только при запуске самого модуля.
7. `main() `: Вызов функции main.

## Задание 3.
### Напишите программу, которая будет выводить текущее время, с точностью до секунд на протяжении 5 секунд. Программу нужно написать с использованием цикла. Подсказка: необходимо использовать модуль datetime и time, а также вам необходимо как-то “усыплять” программу на 1 секунду.
```python
import datetime 
import time 

def main():
    for i in range(5):
        print(datetime.datetime.now().strftime("%H:%M:%S"))
        time.sleep(1)
    
if __name__ == '__main__':
    main()
```
### Результат.
![Задание3с](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/s3.jpg)
## Выводы
1. `import datetime`: Импортируется функция datetime.
2. `import time`: Импортируется функция time.
3. `def main():`: Объявляется функция main().
4. `for i in range(5):`: Цикл. Проходит от 0 до 5.
5. `print(datetime.datetime.now().strftime("%H:%M:%S"))`: Выводит текущее время с в формате ЧЧ-ММ-СС.
6. `time.sleep(1)`: Программа засыпает на 1 секунду.
7. `if __name__ == '__main__':`: Точка входа в программу. Выполняется только при запуске самого модуля.
8. `main() `: Вызов функции main.


## Задание 4.
### Напишите программу, которая считает среднее арифметическое от аргументов вызываемое функции, с условием того, что изначальное количество этих аргументов неизвестно. Программу необходимо реализовать используя одну функцию и “точку входа”.
```python
def main(*args):
    return sum(args)
    
if __name__ == '__main__':
    result = main(12, 4325, 45, 76, 8, 9, 0, 5, 21, 5)
    print(f'result = {result}')
```
### Результат.
![Задание4с](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/s4.jpg)
## Выводы
1. `def main():`: Объявляется функция main().
2. `return sum(args)`: Вызвращает сумму элементов кортежа.
3. `if __name__ == '__main__':`: Точка входа в программу. Выполняется только при запуске самого модуля.
4. `result = main(12, 4325, 45, 76, 8, 9, 0, 5, 21, 5)`: В переменную result записывается функция main c параментрами.
5. `print(f'result = {result}')`: Выводит результат.

## Задание 5.
### Создайте два Python файла, в одном будет выполняться вычисление площади треугольника при помощи формулы Герона (необходимо реализовать через функцию), а во втором будет происходить взаимодействие с пользователем (получение всей необходимой информации и вывод результатов). Напишите эту программу и выведите в консоль полученную площадь
main:
```python
from sup import geron_area
from sup import get_info

def main():
    arr = get_info()
    geron_area(arr[0], arr[1], arr[2])
    

if __name__ == '__main__':
    main()
```
sup:
```python
import math

def geron_area(a, b, c):
    s = (a + b + c) / 2
    print(math.sqrt(s * (s - a) * (s - b) * (s - c)))

def get_info():
    arr = []
    arr.append(float(input("Введите длину стороны a: ")))
    arr.append(float(input("Введите длину стороны b: ")))
    arr.append(float(input("Введите длину стороны c: ")))
    return arrr
```
### Результат.
![Задание5с](https://github.com/Ann-kurbatova/main/blob/Tema4/pic/s5.jpg)
## Выводы
main:
1. `from sup import geron_area`: Импортируется функция geron_area из sup.
2. `from sup import get_info`: Импортируется функция get_info из sup.
3. `def main():`: Объявляется функция main.
4. `arr = get_info()`: В переменную arr записывается значение возвращенное функцией get_info().
5. `geron_area(arr[0], arr[1], arr[2])`: Вызывается функция geron_area() с параметрами.
6. `if __name__ == '__main__':`: Точка входа в программу. Выполняется только при запуске самого модуля.
7. `main()`: Вызов функции main.
sup:
1. `import math`: Импортируется модуль math.
2. `def geron_area(a, b, c):`: Объявляется функция geron_area().
3. `s = (a + b + c) / 2`: Объявляется и присваивается значение переменной.
4. `print(math.sqrt(s * (s - a) * (s - b) * (s - c)))`: Выводит значение формулы герона.
5. `def get_info():`: Объявляется функция get_info().
6. `arr = ()`: Объявляется и присваивается значение переменной.
7. `arr.append(float(input("Введите длину стороны a: ")))`: Добавляет новый элемент в конец списка. Значение элемента будет введенно с клавиатуры. Выводится строка "Введите длину стороны a: ".
8. `arr.append(float(input("Введите длину стороны b: ")))`: Добавляет новый элемент в конец списка. Значение элемента будет введенно с клавиатуры. Выводится строка "Введите длину стороны b: ".
9. `arr.append(float(input("Введите длину стороны c: ")))`: Добавляет новый элемент в конец списка. Значение элемента будет введенно с клавиатуры. Выводится строка "Введите длину стороны c: ".
10. `return arr`: Возвращает значение переменной arr.