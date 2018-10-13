---
title: Compilers
localeTitle: Составители
---
## Составители

### программирование

В основе всего, компьютер с barebone (также известный как программный компьютер) - это не что иное, как машина, которая умеет читать шаги, написанные в фиксированном наборе команд, и выполнять их. Набор инструкций, которые компьютер понимает, очень специфичен для него. Это также называется машинным языком ( **коды операций** ). Язык машины часто упоминается как двоичный код.

Люди взаимодействуют с компьютерами с помощью **программ** . Программа представляет собой просто последовательность кодов операций, предоставляемых компьютеру, а также данные, необходимые для выполнения кодов операций.

Например,
```
ADD 10, 20  // ADD is the Opcode 
            // and 10, 20 are the two operands(data) 
            // needed for the ADD instruction to be executed successfully 
```

Люди разрабатывают программы для решения сложных проблем. Если посмотреть, как работают простые коды операций, если мы попытаемся разработать программы, используя только коды операций, это будет очень громоздко и трудно отлаживать. Для решения этой проблемы были разработаны языки высокого уровня, такие как C / C ++, Python, Java, Javascript и т. Д.

Теперь языки высокого уровня не подходят для выполнения компьютерами. Следовательно, возникла необходимость для переводчика, который может переваривать языковые программы высокого уровня и преобразовывать их в инструкции машинного языка, подходящие для выполнения компьютером.

#### \[ЧЕЛОВЕЧНИКИ\] -> \[Языковые программы на высоком уровне\] -> \[Переводчик\] -> \[Язык машины\] -> \[Компьютер\]

**Компилятор** - это тип программы-переводчика, которая переводит языки высокого уровня в двоичный код, который составляет всего 1 с и 0. Когда вы запускаете исходный код, компилятор сначала переводит весь код, а затем выдает двоичный код. Затем компьютер берет двоичный код и запускает его.

Если в исходном коде имеются ошибки, компилятор обнаруживает и помещает их. Это останавливает процесс компиляции. После исправления всех ошибок компилятор преобразует код и генерирует исполняемую программу.

## Части компилятора

Большинство компиляторов разбиваются на три основных этапа: анализ, преобразование и генерация кода

1.  _Анализ_ делает исходный код и превращает его в более абстрактное представление кода.
2.  _Трансформация_ принимает это абстрактное представление и манипулирует тем, что хочет компилятор.
3.  _Генерация кода_ принимает преобразованное представление кода и превращает его в новый код.

#### анализ

Анализ обычно разбивается на две фазы: **лексический анализ** и **синтаксический анализ** .

_Лексический анализ_ берет необработанный код и разделяет его на эти предметы, называемые токенами, под названием токенизатор (или лексер).
```
Tokens are an array of tiny little objects that describe an isolated piece of the syntax. 
 They could be numbers, labels, punctuation, operators, etc. 
```

_Синтаксический анализ_ принимает маркеры и переформатирует их в представление, описывающее каждую часть синтаксиса и их отношение друг к другу. Это называется промежуточным представлением или абстрактным деревом синтаксиса.
```
An Abstract Syntax Tree, or AST for short, is a deeply nested object. 
 It represents code in a way that is both easy to work with and tells us a lot of information. 
```

#### преобразование

Следующим типом этапа для компилятора является преобразование. Опять же, это просто берет АСТ с последнего шага и вносит в него изменения. Он может управлять АСТ на одном языке или переводить его на совершенно новый язык.

#### Генерация кода

Последней фазой компилятора является генерация кода. Иногда компиляторы будут делать то, что накладывается на трансформацию, но по большей части генерация кода просто берет AST и преобразует ее в двоичный код.

Все компиляторы должны выполнить эти действия. Большинство современных компиляторов также выполняют другие действия, такие как проверка ошибок типа и оптимизация полученного скомпилированного кода.

#### Дополнительная информация:

[Мэтт Адеаньяни «Более внимательное введение в программирование»](https://medium.freecodecamp.org/a-gentler-introduction-to-programming-707453a79ee8) охватывает компиляторы и интерпретаторы, а также другие базовые концепции программирования.