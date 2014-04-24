Про апостроф
------------

Есть в Haskell одна особенность, связанная с именованием. Признаюсь, я удивился, когда о ней узнал. Оказывается, частью имени любой программной сущности может выступать апостроф. Да-да, та самая одинарная кавычка, в которую мы помещаем отдельный символ `Char`.

Мы можем использовать один или более апострофов в имени функции:

```haskell
strangeFunction' :: Int -> Int
strangeFunction' arg = arg
```

в имени типа:

```haskell
data Strange_'type' = Strange_'type' String
```

в имени класса типов:
 
```haskell
class Stran''geClass'' a where
    fmethod :: a -> String
```

и даже в имени значения:
 
```haskell
strangeValue''' :: Integer
strangeValue''' = 123
```

На мой взгляд, включать апостроф в какое-либо имя не нужно вовсе (или очень, очень редко). Тем более что такой символ разрывает текстовую целостность слова (попробуйте выделить двойным кликом идентификатор с апострофом, и вы поймёте). Однако существует практика, в соответствии с которой имя с апострофом в конце используется как "промежуточное имя". Например:

```haskell
let path = "/usr/local/"
    path' = path ++ "lib/"
```

Впрочем, на мой взгляд лучше написать так:

```haskell
let path = "/usr/local/"
    pathWithLib = path ++ "lib/"
```

Кроме того, иногда апостроф может использоваться для придания имени функции, скажем так, большего математического вида. Например, имя производной функции принято писать со штрихом, и в этом случае апостроф вполне подойдёт:

```haskell
f' :: X -> Y
```

Всё. С апострофом вы тоже познакомились.