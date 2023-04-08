# Алгоритмы и структуры данных (лекции)
## Урок 4. Структуры данных дерево и хэш-таблица

### Описание
1. Хэш-таблица. Внутреннее устройство. Оценка сложности поиска.
2. Дерево. Особенности структуры. Сбалансированные деревья. Оценка сложности поиска.
3. Алгоритм обхода (поиска) по дереву сбалансированному и несбалансированному

Видео урока 
https://www.youtube.com/watch?v=sd_7ahFiukY

## Обход дерева в гулбину
Код дерева в глубину [Tree.java](https://github.com/ShumAhd/Lesson-4.-Data-structures-tree-and-hash-table/blob/main/Tree.java)

Самым простым с точки зрения обхода, является обход в глубину. Это рекурсивный
подход к перебору всех значений в дереве, построенный на вызове всех доступных
детей для каждого узла. Таким образом максимальная глубина рекурсии будет
равна максимальной глубине дерева, а порядок будет идти сверху-вниз и
слева-направо
Чаще всего используется именно обход в глубину, т.к. он прост в реализации и не
требует слишком большого количества ресурсов на исполнение.

## Обход в ширину
Код обхода в ширину [Width.java](https://github.com/ShumAhd/Lesson-4.-Data-structures-tree-and-hash-table/blob/main/Width.java)

Обход в ширину предполагает, что мы не обрабатываем детей до тех пор, пока все
родителя одного уровня не были обработаны. Давайте рассмотрим пример, при
котором мы хотим получить все элементы дерева в виде списка
Данный алгоритм не вызывает рекурсию, но в основном используется не для
поиска, а для массовых операций со значениями в дереве

## Бинарное дерево
Код бинарного дерева Binary.java == null

Бинарным деревом называют частный случай дерева, где все элементы
обязательно строго уникальны, каждый родитель имеет не более 2 детей, при этом
левый ребенок всегда меньше родителя, а правый – больше.
Благодаря своим свойствам, бинарные деревья позволяют эффективно
выстраивать поисковые алгоритмы. Находясь на любом из узлов мы всегда точно знаем куда именно нам нужно пойти – налево или направо – чтобы найти искомый
элемент. Алгоритм обхода бинарного дерева происходит в глубину и очень
напоминает алгоритм бинарного поиска


## Сбалансированное дерево
Код сбалансированного дерева Balanced.java == null

Сбалансированным деревом называют частный случай бинарного дерева, у
которого выполняется следующее требование: для любого узла дерева высота его
правого поддерева отличается от высоты левого поддерева не более чем на
единицу.
Таким образом, сбалансированное дерево дает нам идеальную структуру для
бинарного поиска – корень такого дерева — это его центральный элемент –
количество элементов справа и слева от него различается не более чем на
единицу, что характерно для выбора стартовой позиции в бинарном поиске. Таким
образом, сложность поиска по сбалансированному дереву составляет O(log n), что
дает очень высокую производительность.
Для поддержания свойства сбалансированности в процессе операций добавления
или удаления элементов такие деревья должны проводить операции балансировки,
чтобы не допустить разбалансированности и ухудшения сложности поиска.
Существуют различные типы сбалансированных деревьев – АВЛ-дерево,
красно-черное дерево, 2-3 дерево и т.д. Каждое из которых имеет собственные
алгоритмы балансировки. Так, например, для балансировки АВЛ-дерева каждая
нода помимо информации о значении и детях, так же хранит показатель глубины,
на основе которого проводится балансировка по специальному алгоритму. А у
красно-черного дерева вместо показателя глубины используется показатель цвета
– ноды могут быть либо черными, либо красными.
Использование сбалансированных деревьев позволяет создать динамическую
самоддерживаемую структуру, имеющую очень высокую скорость поиска
элементов.

## Красно-Чёрное дерево

[RedBlackTree.java](https://github.com/ShumAhd/Lesson-4.-Data-structures-tree-and-hash-table/blob/main/RedBlackTreeLesson4/RedBlackTree.java)

Код не рисует дерево в терминале, это к сожалению очень нетривиальная задача,
по этому при запуске кода ни чего не произойдёт ))


