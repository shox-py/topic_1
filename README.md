# 1. Начало работы

![img.svg](img%2Fimg.svg)

## Вступление

Добро пожаловать в первую тему по изучению Python! Здесь мы начнем наше увлекательное путешествие в мир
программирования с основ языка.

В этой теме мы поговорим о различных типах данных, которые встречаются в Python, о способах комментирования кода 
и правильной организации кода с помощью отступов.

Не волнуйтесь, если все кажется немного сложным - мы будем постепенно идти вперед, и уверены, что в конце 
обучения вы не только научитесь программировать, но и полюбите этот замечательный язык! 

---

## Содержание:

- [Комментарии](#комментарии)
- [Литералы](#литералы)
- [Числа](#числа)
- [Строки](#строки)
- [Логические и физические строки](#логические-и-физические-строки)
- [Отступы](#Отступы)
- [Преобразование типов часть 1](#преобразование-типов-часть-1)
- [Задания](#задания)

---

## Комментарии

Комментарии в коде - это специальные строковые элементы, которые не выполняются компьютером как код, они предназначены
для пояснения того, что делает код и как он это делает. Комментарии важны, потому что они помогают другим программистам
и вам самим понимать код в будущем.

Хороший комментарий должен быть написан на языке программирования, а не на естественном языке.

_Что это значит?_ Когда вы пишете комментарий на языке программирования, используете термины и синтаксис,
привычные для программистов. Это значит, что другие программисты смогут легче понимать, что вы пытаетесь сделать.

К примеру, вот код на языке Python, который делает простое арифметическое действие:

**Пример**:

```python
a = 2
b = 3
c = a + b
```

Теперь вот тот же код, но с комментариями на языке программирования:

**Пример**:

```python
# Создаем переменную 'a' и присваиваем ей значение 2
a = 2

# Создаем переменную 'b' и присваиваем ей значение 3
b = 3

# Создаем переменную 'c' и присваиваем ей сумму значений переменных 'a' и 'b'
c = a + b
```

а вот плохой комментарий, написанный на естественном языке:

**Пример**:

```python
# Создаем первую переменную
a = 2

# Создаем вторую переменную
b = 3

# Создаем третью переменную и присваиваем ей сумму первых двух переменных
c = a + b
```

Рассмотрим следующий пример, который использует понятие списка `list`:

**Пример**:

```python
numbers = [1, 2, 3]

print(numbers[0])  # 1
```

Комментарий на языке программирования, который объясняет этот код, выглядеть так:

**Пример**:

```python
# Создаем список из трех чисел
numbers = [1, 2, 3]

# Выводим на экран первый элемент списка
# Индексация в Python начинается с 0, поэтому numbers[0] - это первый элемент списка
print(numbers[0])  # 1
```

Этот комментарий помогает объяснить, почему мы используем индекс `0` в квадратных скобках для
получения первого элемента списка. Для человека, знакомого с основами Python, это может быть очевидно,
но для новичка это может быть непонятно.

Вот пример комментарий на естественном языке, который объясняет тот же код:

**Пример**:

```python
# Создаем список
numbers = [1, 2, 3]

# Выводим на экран первый элемент списка
print(numbers[0])  
```

Этот комментарий объясняет, что мы выводим на экран первый элемент списка, но не поясняет, почему мы используем
индекс `0` в квадратных скобках. Это может создать путаницу для читающего и сделать код более сложным для понимания.

Хорошие комментарии - это то, что отличает профессионального программиста от хорошего.

- Не забывайте писать комментарии в своем коде, объясняя свои решения.
- Старайтесь писать комментарии на языке программирования вместо естественного языка, чтобы другие программисты и
  мы сами в будущем могли быстро понять наш код.
- Не стоит писать комментарии там, где сам код достаточно ясен и документирует свою цель. Например,
  если переменная или функция названа так, что её назначение очевидно, добавлять комментарии излишне.

<details><summary>Ещё больше примеров о комментариях</summary>

### Хорошие комментарии

#### Юридические комментарии

Эти комментарии поясняют правовые или лицензионные условия, касающиеся кода или его компонентов.

**Пример**:

```python
# For licensing see accompanying LICENSE file.
# Copyright (C) 2024 Apple Inc. All Rights Reserved.


def some_function():
    pass
```

#### Информативные комментарии

Объясняют сложные участки кода, помогая другим (или вам самим в будущем) быстро понять логику.

**Пример**:

```python
# Используем двоичный поиск, так как список отсортирован, 
# и нам нужно минимизировать количество сравнений.
def binary_search(arr, target):
    left: int = 0
    right: int = len(arr) - 1
    while left <= right:

        middle: int = (left + right) // 2
        if arr[middle] == target:
            return middle
        elif arr[middle] < target:
            left = middle + 1
        else:
            right = middle - 1

    return -1
```

#### Представление намерений

Четко объясняют, что именно пытается сделать данный участок кода, чтобы избежать недоразумений.

**Пример**:

```python
# Преобразуем строку в нижний регистр, чтобы обеспечить 
# корректное сравнение независимо от регистра.
word = word.lower()
```

#### Прояснение

Поясняют, что делает конкретная операция, особенно если она необычная или неочевидная.

**Пример**:

```python
# Преобразуем timestamp в объект datetime для 
# корректного отображения времени.
result = datetime.datetime.fromtimestamp(unix_timestamp)
  ```

#### Предупреждение о последствиях

Указывают на возможные ошибки или побочные эффекты, которые могут возникнуть при изменении кода.

**Пример**:

```python
# Внимание! Если вы измените этот параметр, это может повлиять на 
# производительность, так как требуется пересчитать все кэшированные данные.
cache_size = 1024
```

#### Комментарии `TODO`

Указывают на незавершенные участки кода или задачи, которые необходимо выполнить в будущем.

**Пример**:

```python
# TODO: Реализовать логику сохранения данных
def save_data(data):
    pass
```

#### Усиление

Усиливают важность или необходимость выполнения какого-либо шага в коде.

**Пример**:

```python
# Важно: Эта операция должна быть выполнена до вызова 
# функции save(), иначе данные не сохранятся!
cache.clear()
```

#### Комментарии документации функций или классов

Эти комментарии описывают, как работает функция или класс. Они помогают другим разработчикам или вам
в будущем понять, как использовать функцию или класс, какие аргументы они принимают и что возвращают.

**Пример**:

```python
def get_user_messages(user_id):
    """
    :param user_id: Идентификатор пользователя.
    :return: Список всех сообщений пользователя.
    """
    pass
```

### Плохие комментарии

#### Бормотание

Комментарии, которые добавляются без особой необходимости или с целью просто "отчитаться" о работе.
Они не добавляют ценности.

**Пример**:

```python
# Инициализируем переменную
a = 10
```

#### Избыточные комментарии

Комментарии, которые дублируют очевидное или самодокументируемый код.

**Пример**:

```python
# Умножаем `a` на 2
a = a * 2
```

#### Недостоверные комментарии

Когда комментарий ошибочен, либо не соответствует действительности. Это может сбить с толку других разработчиков.

**Пример**:

```python
# Этот алгоритм работает за O(n) времени
result = insertion_sort()  # на самом деле O(n^2)
```

#### Шум

Комментарии, которые не несут никакой полезной информации, не объясняют логику и только загромождают код.

**Пример**:

```python
def get_day_of_month():
    """Возвращает день месяца."""
    pass
```

#### Комментирование очевидных решений

Комментарии, объясняющие явные или банальные вещи, которые можно легко понять из контекста.

**Пример**:

```python
# Присваиваем переменной значение 100
value = 100
```

#### Использование комментариев для скрытия кода

Иногда разработчики скрывают старый код с помощью комментариев, вместо того чтобы просто удалить его.
Это может привести к путанице и усложнить поддержку.

**Пример**:

```python
result = [1, 2, 3, 4]
# print("Отладочная информация", result)
print(result)  # [1, 2, 3, 4]
```

#### Невыполнимая или устаревшая информация

Комментарии, которые больше не актуальны, например, если решение уже изменилось, но комментарий остался прежним.

**Пример**:

```python
# Используем алгоритм быстрой сортировки, но на самом деле используется слиянием
def merge_sort(arr):
    pass
```

</details>

---

## Литералы

Литералы - это постоянные значения, которые используются для представления фиксированных данных в программе.
Литералы могут быть числами, строками, булевыми значениями или другими типами данных.
В отличие от переменных, литералы не могут изменяться, их значение зафиксировано на момент записи кода.

_Что значит "не изменяются"_? Пример из жизни: в нашем мире существует число `7`, это одно конкретное число,
которое всегда остается одинаковым, где бы мы его не использовали.

**Пример**:

```python
number = 7

result_add = number + 5

result_multi = number * 3
```

В примере выше вы видите, что литерал используется в различных математических операциях.
Вы получаете новые результаты, но сам литерал `7` остается неизменным.
Из этого можно сделать вывод, что числовых литералов существует бесконечно много, да вы будете правы.

Примеры других литералов в Python:

* целые числа: `42` или `-903`;
* числа с плавающей точкой: `3.14`, `9.25E-3` (что равно `0.00925`) или `1E3` (что равно `1000.0`) ;
* строки: в двойных кавычках `"Hello, world!"` или в одинарных `'Привет, мир!'`;
* логические значения: `True` или `False`.
* отсутствие значения: `None`

**Пример**:

``` python
int_literal = 42

float_literal = 3.14159

bool_literal = True

another_bool_literal = False

none_literal = None
```

Если вы плохо поняли пример с литералами чисел, попробуем объяснить это на примере логических значений.
В логическом типе данных всего два литерала: `True` и `False`.

Пример из жизни: представьте выключатель света. Свет может быть либо включен, либо выключен.
В этом случае у нас есть два возможных состояния, и каждое из этих состояний можно назвать литералом.

Теперь, попробуйте ответить на вопрос: _"Сколько литералов у строк?"_

<details>
<summary>
Ответ на вопрос
</summary>
У строк существует бесконечное количество литералов, потому что можно создавать строки с любым количеством символов. 

Например, <code>"pYtHoN"</code>, <code>"Python"</code>, <code>"Привет мир!"</code>, и т.д. - это всё литералы,
и их можно комбинировать в бесконечном числе вариантов.
</details>

---

## Строки

Строковые литералы в Python обычно заключаются в `''` одинарные или `""` двойные кавычки.

**Пример**:

``` python
string_literal = "I want to become a professional programmer"

another_string = 'Я хочу стать профессиональным программистом'
```

Если строковой литерал содержит символ кавычки, который соответствует типу кавычки, используемой для
обозначения самого литерала, то его нужно экранировать обратным слешем `\`.

**Пример**:

```python
string_literal = "She said: \"Hello!\""

another_string = 'It\'s raining outside!'
```

В таких случаях экранирование обратным слешем `\` говорит Python, что символ кавычки не должен
интерпретироваться как конец литерала, а должен быть воспринят как обычный символ строки.

Использования тройных кавычек для создания многострочного строкового литерала:

**Пример**:

```python
long_string = """Это многострочная строка.
Она состоит из нескольких строк,
которые разделены переносами строк.
Также в этой строке можно использовать одинарные и двойные кавычки без экранирования."""
```

В переменную `long_string` присвоили значение многострочной строки, используя тройные кавычки в начале и конце строки.

В этой строке есть несколько строк, разделенных символами переноса строки `\n`.
Важно отметить, что при использовании тройных кавычек символы переноса строки также включаются в создаваемую строку.

Кроме того, внутри строки мы можем использовать как одинарные, так и двойные кавычки без экранирования.

**Пример**:

```python
quote = """Это строка содержит "кавычки" внутри неё."""
```

Если вы хотите разделить длинную строку[^1] на несколько строк[^2] в коде, но не хотите использовать тройные кавычки,
можно воспользоваться круглой скобкой `()` для объединения строк.
Это позволяет разбить строку на несколько строк кода без добавления символа переноса строки.

**Пример**:

```python
zen_of_python = (
    "Явное лучше, чем неявное."
    "Простое лучше, чем сложное."
    "Сложное лучше, чем запутанное."
)

print(zen_of_python)
# Явное лучше, чем неявное.Простое лучше, чем сложное.Сложное лучше, чем запутанное.
```

Обратите внимание, что в данном примере строки объединяются в одну без пробела между ними.
Это происходит потому, что строки, разделённые круглой скобкой, не содержат символа переноса строки
`\n`, и текст выводится как одна строка.

Если вам нужно разделить строки на несколько строк (физических) в коде, но при этом сохранить
переносы строк в выводе, вы должны явно указать символ переноса строки `\n`.

```python
zen_of_python = (
    "Явное лучше, чем неявное.\n"
    "Простое лучше, чем сложное.\n"
    "Сложное лучше, чем запутанное.\n"
)

print(zen_of_python)
# Явное лучше, чем неявное.
# Простое лучше, чем сложное.
# Сложное лучше, чем запутанное.

```

Теперь, в отличие от предыдущего примера, строки разделены на несколько строк (физических) в выводе,
потому что в каждой строке явно указан символ переноса строки.

---

## Числа

**Целые числа:**

Целые числа в Python - это любая последовательность цифр, которую можно использовать в математических операциях.

Целые числа могут быть отрицательными или положительными, но не могут содержать десятичную точку или запятую.
Например, `2`, `42`, `-99` являются целыми числами.

**Числа с плавающей точкой:**

Числа с плавающей точкой в Python, представляют собой числа с десятичной точкой.

Они могут быть положительными или отрицательными, а также использовать экспоненциальное представление
(<code>1.0 * 10 <sup>4</sup></code> `->` `1E4`).

Например, `3.14, 2.0, -0.5` и `1e-3` являются числами с плавающей точкой.

**Комплексные числа:**

Комплексные числа в Python представляются в виде `(реальная часть + мнимая часть * j`), где `j` - мнимая единица.

Реальная часть и мнимая часть могут быть как целыми, так и числами с плавающей точкой.

Например, `(2+3j)` и `(0.5-2.1j)` являются комплексными числами.

```python

# Целые числа
a = 10
b = -5
c = a + b  # 5

# Числа с плавающей точкой
x = 3.14
y = 2.0
z = x * y  # 6.28

# Комплексные числа
m = 2 + 3j
n = 1.5 - 2j
p = m * n  # (3-2.5j)
```

<details>

<summary>Стоит ли использовать комплексные числа?</summary>

Комплексные числа редко бывают необходимы в повседневной разработке.
Например, бэкенд-разработчику, который работает с базами данных,
API или серверной логикой, они скорее всего не будут нужны.

Комплексные числа полезны в областях, где часто встречаются вычисления с изображениями, сигналами,
а также в научных и инженерных расчетах. Если вы решите работать с графикой, обработкой данных
или алгоритмами машинного обучения, вы, возможно, столкнетесь с комплексными числами.

Полезно знать о их существовании и понимать, как с ними работать.
</details>

---

## Логические и физические строки

**Физическая строка** - это строка, как она представлена в исходном коде файла.
В контексте среды разработки или текстового редактора, каждая строка имеет свой порядковый номер,
и каждая из таких строк называется физической строкой.

**Пример**:

```python
1 num = 10
2 print(num)
3
```

В приведенном выше примере, видны три физические строки файла. На первой строке находится выражение `num = 10`,
на второй `print(num)`, а третья строка не содержит логических конструкций.

**Логическая строка** - единое выражение, которое Python рассматривает как одно целое,
даже если оно разделено на несколько физических строк в исходном коде.

**Пример**:

```python
1 total_sum = 10 + \
2 20 + \
3 30
4
```

В этом примере три физические строки представляют собой одно логическое выражение `total_sum = 10 + 20 + 30`.
Несмотря на то, что оно занимает несколько строк в файле, Python рассматривает его как одну логическую строку.

Для удобства и улучшения читаемости кода рекомендуется **использовать круглые скобки** для разделения выражений
на несколько строк, а не символ `\`. Давайте улучшим приведенный выше пример:

**Пример**:

```python
1 total_sum = (10 +
2              20 +
3              30)
4
```

Обычно логическая строка[^3] идентична физической строке, но иногда одна логическая строка может занимать
несколько физических строк.
  
Если вы хотите написать одну логическую строку на нескольких физических строках, можете использовать явное
объединение строк, используя знак обратного слеша <code>&#92;</code> в конце каждой физической строки.

**Пример**:

```python
long_string = "Это длинная строка, которая может занимать \
несколько физических строк. Мы используем знак обратного \
слеша, чтобы Python понимал, что это одна логическая строка."
```

Что если вы хотите записать несколько логических строк в одной физической строке.
Для этого можно использовать точку с запятой `;` для разделения выражений на одной физической строке.

**Пример**:

```python
x = 1; y = 2; z = x + y;
```

Однако, несмотря на возможность использования точки с запятой,
**рекомендуется записывать каждое выражение в отдельной физической строке**, чтобы код был более читаемым и понятным.

Некоторые конструкции, такие как условные операторы и циклы, иногда требуют использования нескольких 
физических строк. В таких случаях необходимо использовать _круглые скобки_ для объединения выражений 
в одну логическую строку.

**Пример**:

```python
if (x > 0
    and y < 10
    and z == 3):
    print("Условие выполнено!")
```

Альтернативный способ - использовать символ `\` для объединения.

```python
if x > 0 \
    and y < 10 \
    and z == 3:
    print("Условие выполнено!")
```

---

## Отступы

В Python отступы играют очень важную роль и используются для определения блоков кода.
Блок кода представляет собой группу команд, которые должны быть выполнены вместе.

Каждый блок кода начинается с новой строки и определяется уровнем отступа.
Один уровень отступа в Python составляет **4 пробела**.
Если уровень отступа в блоке кода не совпадает с уровнем предыдущего блока, то Python выдаст ошибку.

**Пример**:

```python
a = 10
b = 5

if a > b:
    print("a больше, чем b")
else:
    print("b больше, чем a")
```

В данном примере отступы используются правильно. Однако, если мы добавим лишний отступ перед первой строкой, то это
приведет к ошибке:

**Пример**:

```python
    a = 10  # Синтаксическая ошибка
b = 5

if a > b:
    print("a больше, чем b")
else:
    print("b больше, чем a")

```

Ошибка `IndentationError unexpected indent` будет возникать из-за того, что первая строка имеет больше отступов, чем
вторая строка, что не соответствует синтаксису Python.

**Пример**:

```python
a = 10
b = 5

if a > b:
print("a больше, чем b")  # Ошибка из-за отсутствия отступа
else:
    print("b больше, чем a")
```

Или такой вариант, где отсутствуют отступы в блоке `if`, что приводит к ошибке синтаксиса при запуске программы.

---

## Преобразование типов часть 1

В Python существуют специальные функции преобразования, которые позволяют изменять типы данных переменных.
Это полезно, когда нам нужно выполнить определенные операции или работать с данными определенного типа.

Встроенные функции преобразования типов:

* `float()` - используется для преобразования значения в число с плавающей точкой;
* `int()` - используется для преобразования значения в целое число;
* `str()` - используется для преобразования значения в строку;
* `complex()` - используется для создания комплексного числа.

Могут принимать один аргумент (значение, которое нужно преобразовать) и возвращать результат
в виде значения другого типа.

**Пример**:

```python
a = 5
b = 2

# float() - преобразует значение в десятичную дробь
c = float(a) / b
print(c)  # 2.5

# int() - преобразует значение в целое число
d = int(c)
print(d)  # 2

# str() - преобразует значение в строку
e = str(d)
print(e)  # "2"

# complex() - создает комплексное число
f = complex(a, b)
print(f)  # (5 + 2j)
```

Преобразование типов данных - это процесс изменения типа значения переменной из одного в другой тип.

**Пример**:

```python
a = 5.7

b = int(a)  # b будет равно 5, дробная часть отбрасывается
c = str(b)  # c будет равно "5"

d = "3.14"

e = float(d)  # e будет равно 3.14
```

Обратите внимание, что при попытке преобразовать строку, содержащую число с плавающей точкой,
в целое число с помощью функции `int()` возникнет ошибка.

**Пример**:

```python
int("3.14")  # ValueError: invalid literal for int() with base 10: '3.14'
```

Чтобы решить эту проблему, нужно сначала преобразовать строку в число с плавающей точкой, а затем в целое число.

**Пример**:

```python
int(float("3.14"))  # 3
```

Если вы попытаетесь преобразовать значение, которое невозможно привести к целому числу, например строку, содержащую
буквы или другие нечисловые символы, возникнет исключение `ValueError`.

**Пример**:

```python
int('abc')  # ValueError: invalid literal for int() with base 10: 'abc'
```

Аналогично, если вы попытаетесь преобразовать строку, которая не является корректным представлением
числа, используя функцию `float()`, также будет сгенерировано исключение `ValueError`.

**Пример**:

```python
float('abc')  # ValueError: could not convert string to float: 'abc'
```

Функция `str()` используется для преобразования любого объекта в строковое представлени.

**Пример**:

```python
a = 5
b = str(a)  # b будет равно "5"
c = str(3.14)  # c будет равно "3.14"
d = str(True)  # d будет равно "True"
e = str(None)  # e будет равно "None"
```

---

## Заключение

Надеемся, что вы получили много новых знаний о том, как работать с Python.
Вы узнали основные принципы языка и теперь готовы к новым вызовам.
Это только начало вашего путешествия, и впереди много интересных тем и возможностей для развития.

Мы рады, что вы к нам присоединились! В следующей теме мы научимся работать с консолью и 
начнем создавать свои первые программы!

---

## [Задания](./tasks/TASKS.md)

Практические задания для самостоятельной работы.

- Постарайтесь использовать только те знания, которые были изучены в пройденных темах.
- Не стоит использовать f-строки и т.п., если мы ещё не разбирали их.
- Убедитесь, что удалили все лишние комментарии из вашего кода.
- Рекомендуем решить все задания самостоятельно.

Если возникнут трудности, не стесняйтесь обращаться за помощью в наш [Телеграм-чат](https://t.me/shox_py_discuss).
Чтобы перейти к заданиям, кликните на заголовок **Задания** или нажмите [сюда](./tasks/TASKS.md).

---

## Полезные ссылки

- [Best practices for writing code comments](https://stackoverflow.blog/2021/12/23/best-practices-for-writing-code-comments/)
- [Python Data Types](https://www.w3schools.com/python/python_datatypes.asp)

---

## Рекомендуемые книги

- [Основы Python. Научитесь думать как программист](https://www.litres.ru/book/allen-b-dauni/osnovy-python-nauchites-dumat-kak-programmist-64838906/)

---

[^1]: **Строка** - тип данных в Python, который представляет собой последовательность символов.
[^2]: **Физическая строка** - это строка, как она представлена в исходном коде файла.
[^3]: **Логическая строка** - единое выражение, которое Python рассматривает как одно целое, 
даже если оно разделено на несколько физических строк в исходном коде.
