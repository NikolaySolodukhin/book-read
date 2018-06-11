1) `Сложность алгоритма` оценивается как `O(n)` где `n` количество операций

`O (log n)` - бинарный поиск. Для его осуществления массив должен отсортирован.

Бинарный поиск работает намного быстрее простого.

`O (n log n)` - эффективный алгоритм сортировки

Пример долгого алгоритма Задача коммивояжёра `O(n!)`


2) `Рекурсия` 

Рекурсия - вызов функцией самой себя. В каждой рекурсивной функции `обязательно` должно быть `два` случая: базовый и рекурсивный. В рекурсивном случае функция вызывает сама себя. В базовом случае себя не вызывает, чтобы предотвратить зацикливание.

3) `Стек` - абстрактный тип данных, представляющий собой список элементов, организованный по принципу `LIFO` (*last in - first out*). Стек поддерживает всего два действия: занесение (вставка) и извлечение(выведение из списка и чтение).

Все вызовы функций сохраняются в стеке вызовов.


3) `Стратегия разделя и властвуй` - 

Сначала определяется базовый случай. Это должен простейший случай из всех возможных.

Задача делится или сокращается до тех пор, пока не будет сведена к базовому случаю. 

Алгоритм быстрой сортивроки:

a) Сначала выбирается элемент, который называется опорным

б) Находим элементы меньше и больше опорного

в) Рекурсивно применить быструю сортировку к двум подмассивам 

Сравнение сортировка слиянием и быстрой сортировки. 

Сортировка слиянием `всегда` работает за время `O(n log n)`.

Быстрая сортировка в худшем случае работает за O (n<sup>2</sup>)

Дело в том, что скорость определяют `O(n)`, однако это означает следующее `c*n`, где c некоторый фиксированный промежуток времени для вашего алгоритма. Константа обычно игнорируется. Однако в некоторых случаях константа `может иметь` значение. Например, быстрая сортировка и сортировка слиянием. У быстрой сортировки константа меньше, чем у сортировки слиянием. Поэтому несмотря на то, что оба алгоритма имеют сложность `O(n log n)`, быстрая сортировка работает быстрее, так как средний случай встречается намного чаще худшего.


Если вы реализуете алгоритм быстрой сортировки, выберите в качестве опорного элемента случайный элемент. Среднее время выполнения быстро сортировки составит O(n log n).

Константы в О-большом иногда имеют большое значение.

4) `Граф`- абстрактная схема моделирующая набор связей.

Каждый граф состоит из `узлов` и `ребер`. 

Графы используются для моделирования связей между разными объектами.

Поиск в ширину (BFS - Breadth First Search). 

Данный алгоритм позволяет ответить на следующие вопросы: 

1) Существует ли путь от узла А к узлу В? 

2) Как выглядит кратчайший путь от узла А к узлу В? 

Очередь. 

Очередь относится к категории структур данных FIFO: First In, First Out. 

Поиск в ширину выполняется за время O(количество вершин + количество ребер).

5. `Алгоритм Дейкстры` - алгоритм при помощи которого можно найти кратчайший путь в графе.

1) Найти узел с наименьшей стоимостью (до которого можно добраться за минимальное время)

2) Обновить стоимость соседей этого узла

3) Повторить пока это не будет сделано для всех узлов графа

4) Вычислить итоговый путь 

Когда мы работаем с алгоритмом Дейкстры с каждым ребром графа связывается его число - `вес графа`.

Очевидные очевидности сейчас напишу, ну пусть будет.

Граф с весами - `взвешенные` граф.

Граф без весов - `невзвешенный` графом. 

Для вычисления кратчайшего пути в невзвешенном графе используется поиск в ширину. Кратчайшие пути во взвешенном графе вычисляются по алгоритму `Дейкстры`. 

В графах могут присутствовать циклы. 
В ненаправленном графе каждое новое ребро добавляет еще один цикл. 

Алгоритм `Дейкстры` работает только с направленными ациклическими графами DAG (Directed Acyclic Graph).

Использование алгоритма `Дейкстры` с графом содержащим ребра с отрицательным весом, невозможно. Для этого случая есть алгоритм `Беллмана - Форда`. 


5) Жадные алгоритмы.

Жадные алгоритмы стремятся к локальной оптимизации в расчете на то, что в итоге будет достигнут глобальный оптимум.


NP-полные задачи

Признаки NP сложных задач:

1) Ваш алгоритм быстро работает при малом количестве элементов, но сильно замедляется при увеличении их числа

2) Формулировка `все комбинации X` часто указывает на NP-полноту задачи

3) Вам приходится вычислять все возможные варианты X, потому что задачу невозможно разбить на меньшие подзадачи.

4) Если в задаче встречается некоторая последовательность (напримре последовательность городов, как в задаче о коммивояжере) и задача не имеет простого решения, она может оказаться NP-полной 


5) Если в задаче некоторое множество (например множество радиостанций) и задача не имеет просто решения, она может оказаться NP-полной


Если NP-задача то лучше воспользоваться жадным алгоритмом - быстро реализуется и быстро выполняется в итоге получается хороший приближенный алгоритм.


6) Динамическо программирование

a) Динамическое программирование применяется при оптимизации некоторой характеристики

б) Динамическое прогарммирование работает только в ситуациях, в которых задача может быть разбита на автономные подзадачи

в) В каждом решении из области динамического программирования строится таблица

г) Значения ячеек таблицы обычно соотвествует оптимизируемой характеристике

д) Каждая ячейка представляет подзадачу, поэтому вы должны подумать о том, как разбить задачу на подзадачи

e) Не существует единой формулы для вычисления решений методом динамического програмирования


7) `Алгоритм k-ближайших соседей`

Алгоритм k ближайших соседей применяется для классификации и регрессии. 

В нем используется проверка k ближайших соседей. 

Классификация - распределение по категориям.

Регрессия - прогнозирование результата.


Обзор `других` <span style="color:red">важных алгоритмов</span>


a) Параллельные алгоритмы. Лучшее время выполнения для алгоритма сортировки приблизительно `O(n log n)`. Известно, что массив невозможно отсортировать за время `O(n)`, но что если воспользоваться параллельным алгоритмом. Есть версия параллельная версия быстрой сортировки, которая сортирует массив за время `O(n)`.

Выигрыш по времени не линеен. Следовательно е
сли процессор имеет два ядра вместо одного из этого не следует, что скорость алгоритма будет быстрее в два раза. 

При разработке паралельного алгоритма важно учитывать:

a1) `Затраты ресурсов на управление парллелизмом`. Допустим нужно отсортировать массив из 1000 элементов. Как разбить эту задачу для выполнения на двух ядрах? Плюс вопрос о слиянии массивов требует времени.

a2) `Распределение нагрузки` - возникает вопрос как организовать равномерное распределение работы, чтобы оба ядра трудились с одинаковой интенсивностью. 

Одной из разновидностью параллельных алгоритмов в последнее время становятся - распределенные алгоритмы. Алгоритм MapReduce - известный представитель семейства распределенных алгоритмов. В `основе` MapReduce лежат две простые идеи(забавно читать про это когда знаешь методы map и reduce для массивов): функция отображения map и функция свертки reduce. 

MapReduce использует две простые концепции для выполнения запросов на нескольких машинах.

Также для работы с большими данными например чтобы хранить большое количество страниц. Можно использовать хеш-таблицы, однако хеш таблица будет занимать очень много памяти. Для более элегантного решения проблемы существуют фильтры `Блума` и `HyperLogLog`. 

Фильтры Блума - вероятностная структура. Она дает ответ, который может показаться ложным, но с большой вероятностью является правильным. 

В фильтрах Блума возможны ложно-положительные срабатывания. 

Ложно отрицательные срабатывания исключены. `Ключевая фича фильтров Блума` - они занимают `намного меньше памяти`, чем хэш-таблицы.

Фильтр блума оказался интересным включу и его сюда:

Фильтр Блума представляет собой битовый массив из m бит. Изначально, когда структура данных хранит пустое множество, все m бит обнулены. Пользователь должен определить k независимых хеш-функций h1, …, hk, отображающих каждый элемент в одну из m позиций битового массива достаточно равномерным образом.

Для добавления элемента e необходимо записать единицы на каждую из позиций h1(e), …, hk(e) битового массива.

Для проверки принадлежности элемента e к множеству хранимых элементов, необходимо проверить состояние битов h1(e), …, hk(e). Если хотя бы один из них равен нулю, элемент не может принадлежать множеству (иначе бы при его добавлении все эти биты были установлены). Если все они равны единице, то структура данных сообщает, что е принадлежит множеству. При этом может возникнуть две ситуации: либо элемент действительно принадлежит множеству, либо все эти биты оказались установлены по случайности при добавлении других элементов, что и является источником ложных срабатываний в этой структуре данных.

Алгоритм LogLog и HyperLogLog довольно сложны). Ознакомлюсь с ними позже <a href="http://dimchansky.github.io/posts/2014/10/20/cardinality-estimation-using-hyperloglog/">тут</a>.


Обмен ключами Диффи-Хеллмана(криптография) и симплекс метод(линейное програмирование) оставим для дальнейшего изучения.

