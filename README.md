Что ж... по данным запуска main, можно понять, что медленнее всего исполняется алгоритм "в лоб" не понятно, как исполняется api (имею ввиду, что там по сложности внутри api), но в худшем случае api исполнится три раза, если в id попал город принадлежащей области

Второй алгоритм "перебора дерева" выполняется быстрее, могу предположить, что получение всех адресов занимает меньше времени, чем получение простой ноды адреса. Но сложность алгоритма выше. В худшем случае O(n^3)

Третий алгоритм с мемоизацией работает быстрее всех. Так как сначала идёт инициализация (но ведь замеряли конктретное декодирование id в адрес), а потом за константное время происходит поиск адреса по id.

По памяти предположу, что эффективность будет обратная - 1, 2, 3. В первом ничего не сохраняется. Во втором сохраняется дерево адресов. В третьем происходит распаковка и сохранение дерева в словарь.

Буду рад, если дадите обратную связь.

