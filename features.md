---
title: Features
layout: default
---
## Функции языка, которые мы реализовали
- [+] Именованные переменные (`var`)
- [+] Рекурсия
- [+] Ленивые вычисления
- [+] Функции
- [+] Замыкания
- Дополнительно комментарии

## Булевые выражения
Используются две логические операции: оператор "AND" (представлен символом `&`) и оператор "OR" (представлен символом `|`). 
Логические константы true и false записываются в нижнем регистре и без кавычек.

Аргументы функции могут быть как логическими, так и числовыми переменными. 
Преобразование числовых переменных в логические выполняется подобно большинству языков программирования: 
`0` интерпретируется как `false`, все остальное - как `true`.

**Примеры:**
```
(& 1 1) # true
(| 0 0) # false
(& 0 1) # false
(| 0 1) # true
(| true false) # true
```

## Реляционные операторы 
Добавили операторы `<`, `>` и `=`.
На вход подаются 2 значения (числа, строки и булевые), результат  `true` или `false`. 
Можно производить сравнение между числами, строками и булевыми значениями.

**Примеры**
```
  (= false true) # false
  (< 666 1) # false
  (> 10 5) # true
  (& true (< 10 1)) # false
```

## Литералы 
Литералы должны быть заключены в кавычки

**Примеры**
```
 ("string example")
```

## Именованные переменные 
Именованные переменные задаются не через `let`, а через `var`

**Примеры**
```
(var id "string example")
(var id (+ 5 2))
```

## Функция печати
`sout` - функция вывода в стандартный поток вывода
**Примеры**
```
(sout "example")
```

## Функции
Синтаксис: `(def function_name { arg1 arg2 arg3 } (Expr))`. Название функции и ее аргументы представлены 
неотделимыми строками без кавычек и могут быть без аргументов. Когда функция вызывается, 
система проверяет количество аргументов и сопоставляет с параметрами функции. 
Из-за возможности замыканий любая функция может стать рекурсивной. 
Итоговое возвращаемое значение от функции представляется как Expr.SIMPLE.
**Примеры**
```
(def factorial {n}
    (if (= n 0)
        then 1
    else (* n (factorial (- n 1)))
    )
)
(sout (factorial 1))
```

## Комментарии
`#` - Однострочные комментарий \
`$...$` - подобие многострочного комментария 

**Примеры**
```
(var id "string example") # пример комментария
```

## Условные операторы
Для создания условного выражения можно использовать следующий синтаксис: `(if Expr then Expr else Expr)`. При выполнении сначала будет оцениваться выражение, находящееся после if. Возвращаемым значением будет Expr.

Обратите внимание
Элемент else необязателен. Если его не указать, будет использовано значение `Expr.SIMPLE`
**Условные выражения**
```
(if (= number 10)
    then ((sout "eq")
else "not eq")
```
