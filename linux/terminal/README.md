# terminal

## Гарячі клавіши

<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>T</kbd> — відкрити новую вкладку;

<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>N</kbd> — відкрити новое окно

<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>W</kbd> або <kbd>Ctrl</kbd>+<kbd>D</kbd> — закрити поточну вкладку (или весь терминал, если вкладка одна);

Якщо вкладок багато, тоді виникне питання навігації між ними. Вам знадобляться наступні клавіші:

<kbd>Ctrl</kbd>+<kbd>PgDn</kbd> — перейти на следующую (справа) вкладку;

<kbd>Ctrl</kbd>+<kbd>PgDn</kbd> — перейти на предыдущую (слева) вкладку;

<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>PgDn</kbd> — сдвинуть вкладку вправо;

<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>PgUp</kbd> — сдвинуть вкладку влево.

<kbd>Alt</kbd>+<kbd>1</kbd> — перейти на першу за підрахунком вкладку. Підставте іншу цифру для потрібної вкладки. Цей спосіб дозволяє «дотягнутися» максимум до десятої вкладки.

### Навігація

Три комбінації, що використовуються найчастіше для копіювання та вставки тексту, а також скасування команди, що виконується:

<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>С</kbd> — копіювання в буфер обміну;

<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>V</kbd> — вставка з буфера обміну;

<kbd>Ctrl</kbd>+<kbd>C</kbd> — переривання команди, що виконується, або очищення поточного рядка.

Щоб виділити потрібний текст у терміналі, вам потрібно скористатися мишею. Тим не менш, у програмі «Термінал Gnome» є вбудований засіб пошуку тексту, який дозволяє шукати як за звичайним фрагментом, так і за регулярним виразом:

<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>F</kbd> — виклик вбудованого пошуку за будь-яким текстом у терміналі.

Якщо команда в терміналі занадто довга, або ви зробили помилку на початку і не відразу це помітили, ви можете повернутися на початок рядка. А потім знову в кінець. Ось як це зробити:
<kbd>Ctrl</kbd>+<kbd>A</kbd> — переместиться в начало строки;

<kbd>Ctrl</kbd>+<kbd>E</kbd> — переместиться в конец строки.

В терминале Linux можно перемещаться внутри строки также по словам и по отдельным символам (в последнем случае, это аналогично использованию клавиш с боковыми стрелками):

<kbd>Ctrl</kbd>+<kbd>F</kbd> — переместиться на 1 символ вперед;

<kbd>Ctrl</kbd>+<kbd>B</kbd> — переместиться на 1 символ назад;

<kbd>Alt</kbd>+<kbd>F</kbd> — переместиться к следующему слову;

<kbd>Alt</kbd>+<kbd>B</kbd> — переместиться в начало предыдущего слова.

### Управление командами и процессами

Предыдущие команды касались навигации по терминалу и строке ввода команды. Далее стоит рассмотреть управляющие команды Bash, с помощью которых можно запускать, останавливать, ставить на паузу и возобновлять команды и процессы. Вы уже знаете, что запущенный в терминале процесс можно прервать по <kbd>Ctrl</kbd>+<kbd>C</kbd>, но полезно также знать и некоторые нюансы.

В терминале Linux вы можете не только завершать программы полностью, но и ставить их на паузу. Затем выполнение программы можно возобновлять, причем, как с возвратом интерактивной командной строки, так и без него:

<kbd>Ctrl</kbd>+<kbd>Z</kbd> — приостановка процесса;

команда **bg** — возобновление процесса с возвратом командной строки (процесс продолжает выполнение в фоне);

команда **fg** — возобновление процесса, при котором он удерживает командную строку за собой (процесс выполняется на «переднем плане»).

Процессы также можно приостанавливать и возобновлять. Запустите какую-либо команду, например htop, и нажмите <kbd>Ctrl</kbd>+<kbd>Z</kbd>. Сначала будет казаться, будто команда завершилась, но она будет числиться в списке запущенных процессов (`ps -a`) и появится вновь после ввода команды **fg**.

Если повторить эксперимент с графическим приложением, например, введя команду **firefox**, то можно будет использовать для его «оживления» как **fg**, так и **bg**. При любом варианте приложение останется «закрепленным» за текущим терминалом: если вы закроете его, то оно тоже завершится.

Якщо повторити експеримент із графічним додатком, наприклад, ввівши команду **firefox**, то можна буде використовувати для його "пожвавлення" як **fg**, так і **bg**. За будь-якого варіанта додаток залишиться «закріпленим» за поточним терміналом: якщо ви закриєте його, воно теж завершиться.

Существует и другой тип «приостановки»: временное прекращение вывода выполняющейся команды. Как консольное, так и графическое приложение может быть запущено в терминале, в который будет выводиться текущая диагностическая информация. Иногда бывает очень удобно временно прекратить постоянный вывод сообщений без завершения самого приложения. Для этого пригодятся следующие сочетания клавиш:

Існує й інший тип «призупинення»: тимчасове припинення виведення команди, що виконується. Як консольний, так і графічний додаток може бути запущений у терміналі, в який виводитиметься поточна діагностична інформація. Іноді буває дуже зручно тимчасово припинити постійний виведення повідомлень без завершення програми. Для цього знадобляться наступні клавіші:

<kbd>Ctrl</kbd>+<kbd>S</kbd> — прекратить обновление вывода команды;

<kbd>Ctrl</kbd>+<kbd>Q</kbd> — возобновить вывод команды.

### История команд

Bash умеет запоминать все введенные вами команды. Пока терминал запущен, они хранятся в оперативной памяти компьютера, а при выходе из терминала записываются в долговременное хранилище в файле `~/.bash_history`.

Если вы точно знаете, что вводили нужную вам команду раньше, поищите ее в истории:

**history** — вывод истории команд;

Если вы помните хотя бы часть команды, поиск можно уточнить:

```history | grep <часть команды>``` — пример уточняющего поиска по истории командам.

У каждой команды в истории есть номер. Введите этот номер, поставив вначале восклицательный знак, и Bash выполнит соответствующую команду:

<kbd>!151</kbd> — выполнить команду под номером 151 из истории;

<kbd>!151:</kbd> — показать команду номер 151, но не выполнять ее;

<kbd>!!</kbd> — повторно выполнить последнюю введенную команду.

В Bash имеется интерактивный режим поиска по истории команд. Нажмите <kbd>Ctrl</kbd>+R и начните набирать часть команды. Bash сам предложит вам первый совпадающий вариант. Если он не подходит, нажимайте <kbd>Ctrl</kbd>+<kbd>R</kbd> дальше для перебора вариантов. Когда нужный вариант будет найден, нажмите Enter.

Интересно, что у этой клавиши ввода есть два аналога — вместо Enter можно нажать <kbd>Ctrl</kbd>+<kbd>M</kbd> или <kbd>Ctrl</kbd>+<kbd>J</kbd>.

Самый простой способ перемещаться по истории команд — стрелки «вверх» и «вниз» на клавиатуре. Они тоже имеют дубликаты:

<kbd>Ctrl</kbd>+<kbd>P</kbd> — вывести предыдущую команду;

<kbd>Ctrl</kbd>+<kbd>N</kbd> — вывести следующую команду.

### Редактирование команд

Самое время рассмотреть средства редактирования команд — они в Bash весьма продвинутые. Удобное перемещение в начало и конец строки, выборочное удаление символов и слов — это лишь часть возможностей, которые могут пригодиться пользователю. За редактирование команд отвечают следующие сочетания клавиш:

<kbd>Ctrl</kbd>+<kbd>U</kbd> — удалить весь текст слева от курсора;

<kbd>Ctrl</kbd>+<kbd>K</kbd> — удалить весь текст справа от курсора;

<kbd>Ctrl</kbd>+<kbd>W</kbd> — удалить 1 слово или параметр слева от курсора;

<kbd>Ctrl</kbd>+<kbd>D</kbd> — удаление текущего символа (аналогично Del);

<kbd>Ctrl</kbd>+<kbd>H</kbd> — удаление предыдущего символа (аналогично Backspace);

<kbd>Alt</kbd>+<kbd>D</kbd> — удалить все справа от курсора до ближайшего пробела;

<kbd>Alt</kbd>+<kbd>Backspace</kbd> — удалить все слева от курсора до ближайшего пробела;

<kbd>Alt</kbd>+<kbd>T</kbd> — поменять местами текущее слово с предыдущем;

<kbd>Esc</kbd>+<kbd>T</kbd> — поменять местами два предыдущих слова;

<kbd>Tab</kbd> — автодополнение команды после ввода ее первых символов.

Еще одна любопытная деталь: у Bash имеется собственный буфер обмена, который работает независимо от стандартного буфера (как мы помним, копирование по <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>C</kbd>, вставка по <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>V</kbd>). Это важно, поскольку у первых трех команд из предыдущего списка есть дополнительные функции: они не просто удаляют часть текста, но и копируют его в тот самый отдельный буфер обмена Bash. Поэтому, будет справедливо уточнить:

<kbd>Ctrl</kbd>+<kbd>U</kbd> — вырезать и поместить в буфер обмена весь текст слева от курсора;

<kbd>Ctrl</kbd>+<kbd>K</kbd> — вырезать и поместить в буфер обмена весь текст справа от курсора;

<kbd>Ctrl</kbd>+<kbd>W</kbd> — вырезать и поместить в буфер обмена 1 слово или параметр слева от курсора;

Кстати, для вставки скопированного текста обратно сработает комбинация <kbd>Ctrl</kbd>+<kbd>Y</kbd>.

### Напоследок

Конечно, выше я описал не все горячие клавиши: их гораздо больше, и полное описание содержало бы в себе кучу бородатой экзотики, унаследованной из древних университетских времен UNIX. В любом случае, не забывайте про `man bash` (например, там есть замечательный раздел Commands for Moving) и про `bind -P`.

keys: hot keys | keyboard shortcuts

<https://habr.com/ru/post/663758/>
