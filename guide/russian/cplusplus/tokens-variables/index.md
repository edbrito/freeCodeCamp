---
title: Tokens Part 1
localeTitle: Токены Часть 1
---### Что такое токены?

Токены - это наименьшие единицы программы, которые важны для компилятора. Существуют различные виды токенов:

*   Ключевые слова
    
*   операторы
    
*   знаки пунктуации
    
*   литералы
    
*   Идентификаторы
    
*   **Сочетание токенов формирует выражение**
    

### Что такое переменные?

*   Определение учебника: переменные называются ячейками памяти, данные которых могут быть изменены.
    
*   Но я хотел бы, чтобы вы подумали, что переменная будет чем-то вроде коробки, что-то вроде этого: ![Img](https://i.imgur.com/YdbgWHL.png)
    

Так, например: Я перехожу на новое место, и мне нужно укладывать вещи в коробки. Таким образом, мне приходят две вещи. **Какие вещи будут храниться в ящике, так что размер с поля известен (тип данных)** и **как я могу определить поле? (Именование переменной)**  
Следовательно, мы знаем, что переменная в C ++ нуждается в _имени_ и _типе данных_ и что значение, хранящееся в них, может быть изменено.

### Типы данных в C ++:

При объявлении переменных в c ++ у них должно быть имя, на которое вы позже будете ссылаться, значение (константа или нет) и тип. Тип подскажет компилятору значения, которые может использовать переменная, возможные операции и сохранит определенное пространство в memmory. В c ++ существуют два типа данных:

*   Простой тип
*   Тип структуры

### Простые типы данных

*   Boolean - bool Работает как переключатель, может быть включен или выключен.
*   Символ - символ Сохраняет один символ.
*   Integer - int Сохраняет [целое число](https://en.wikipedia.org/wiki/Integer) .
*   Плавающая точка - поплавок Они могут использовать десятичные знаки.
*   Двойная плавающая точка - двойная Двойная точность поплавкового типа.

Здесь вы можете увидеть несколько примеров:

```cpp
bool GameRunning = true; 
 char a; 
 int x = 2; 
```

#### Эти типы также могут быть изменены с помощью таких модификаторов, как:

подписанный неподписанный короткая длинный

### Тип данных структуры

#### Идентификаторы.

*   Идентификаторы - это имена, присвоенные переменной или классу или функции или любой функции, определенной пользователем.

## Правила для именования переменной:

*   Начните именовать буквой из AZ или az.
*   Числа могут следовать за первой буквой, но мы не можем начинать именовать цифры.
*   НЕТ использования пробелов или специальных символов, вместо этого используйте UNDERSCORE \_.

#### Объявление переменной:

Синтаксис выглядит следующим образом < _тип данных_ > < _имя переменной_ >; или < _тип данных_ > < _имя переменной_ > = < _значение_ >; если мы также хотим инициализировать переменную.

Например : `cpp int a ; //declaring a variable named 'a' of type integer. a=4; //initializing a variable int b = 5 ; //declaring and initializing a variable 'b' of type integer.`

**Примеры объявления переменной:**

```cpp
int a9; 
 char A; 
 double area_circle; 
 long l; 
```

**Неправильные способы объявления переменных** -

```cpp
int 9a; 
 char -a; 
 double area of circle; 
 long l!!; 
```

*   Имена переменных не могут начинаться с числа
*   Спецсимволы не допустимы
*   Пробелы не допускаются

Вы можете представить себе различные коробки разных размеров и хранить разные вещи как разные переменные.

**ЗАМЕТКИ :**

1.  **Компилятор C ++ игнорирует пробелы, и они обычно используются для улучшения кода, так что любой программист может отлаживать или понимать код.**
2.  **Если переменная не инициализирована, она содержит значение мусора. Позвольте мне привести пример:**

### Объем переменных

Все переменные имеют свою область функционирования, и из этой границы они не имеют своей ценности, эта граница называется областью действия переменной. В большинстве случаев его между фигурными фигурными скобками, в которых объявляется переменная, существует переменная, а не вне ее. Мы изучим классы хранения позже, но на данный момент мы можем разделить переменные на два основных типа,

\* Глобальные переменные.

\* Локальные переменные.

#### Глобальные переменные

Глобальные переменные - это те, которые объявлены и могут использоваться на протяжении всего жизненного цикла программы любым классом или любой функцией. Они должны быть объявлены вне функции main (). Если объявлено только, они могут быть назначены разные значения в разное время в жизни программы. Но даже если они объявлены и инициализированы одновременно за пределами функции main (), тогда также им может быть присвоено любое значение в любой точке программы.

Пример: Только объявлено, а не инициализировано.

```cpp
#include <iostream> 
 using namespace std; 
 int x;                // Global variable declared 
 int main() 
 { 
 x=10;                 // Initialized once 
 cout <<"first value of x = "<< x; 
 x=20;                 // Initialized again 
 cout <<"Initialized again with value = "<< x; 
 } 
```

#### Локальные переменные

Локальные переменные - это переменные, которые существуют только между фигурными фигурными скобками, в которых объявлено. Снаружи они недоступны и приводят к ошибке времени компиляции.

Пример :

```cpp
#include <iostream> 
 using namespace std; 
 int main() 
 { 
 int i=10; 
 if(i<20)        // if condition scope starts 
  { 
    int n=100;   // Local variable declared and initialized 
  }              // if condition scope ends 
 cout << n;      // Compile time error, n not available here 
 } 
```

### Константные переменные

Константная переменная - это переменные, которые нельзя изменить. Например, если вам нужен «pi» в вашем коде, вы не захотите изменить его после инициализации.

Пример :

```cpp
#include <iostream> 
 using namespace std; 
 const double PI = 3.14159253; 
 int main() 
 { 
 //Calculating the area of a circle, using user provided radius 
 double radius; 
 //input and output explained in other guide 
 cin>>radius; 
 //pi*r^2 
 double area = PI*radius*radius; 
 cout<<area<<endl; 
 } 
```

### Значения мусора в переменной

Если переменная не инициализирована, она содержит значение мусора. Например:

Итак, с точки зрения ящиков, вы можете представить это как -

![Img](https://i.imgur.com/YdbgWHL.png)

\`\` \`Каст #включают использование пространства имен std; int main () { int a; cout << "Значение мусора в a:" << a << endl; // объявляем переменную с именем 'a' типа integer а = 5; // инициализация переменной. cout << "Новое значение в" << a << endl;

} \`\` \`

### Выход:
```
Garbage value in a : 0 
 New value in a :  5 
```

Как вы можете видеть, уже есть значение, хранящееся в 'a', прежде чем мы дадим ему значение (здесь оно равно 0). Это должно оставаться в памяти каждого программиста, чтобы при использовании переменных они не создавали логическую ошибку и не печатали значения мусора.

[Попробуйте код самостоятельно! :)](https://repl.it/Mg7j)

#### Ключевые слова:

_Ключевые слова - это зарезервированные слова, которые передают особый смысл компилятору. Они **НЕ МОГУТ** использоваться для именования в c ++._ Примеры ключевых слов: inline, operator, private int, double, void, char, template, using, virtual, break, case, switch, friend и т. д.

**Каждое из этих ключевых слов используется для специальной функции в C ++.**

_Токены часть 1 закончена. Увидимся в палатках во [второй](https://guide.freecodecamp.org/cplusplus/tokens-part-II) части токенов :)_

**Удачи всем вам**

**Счастливое кодирование! :)**

**Не стесняйтесь задавать любые вопросы на странице GitHub [FreeCodeCamp](https://forum.freecodecamp.org/) или [форуме FreeCodeCamp.](https://forum.freecodecamp.org/)**