# Linux. Команды

- `clear` - очищает окно терминала, или <kbd>Ctrl</kbd>+<kbd>L</kbd>
- `reset` - восстановить исходные параметры окна терминала

<span class="warn">TODO!</span> посмотри <http://www.linux-ink.ru/static/SL.5.1_Docs/Russification/Docs/sbs-sl-ru/index.html> пункт 4 

[сбросить и снова включить своп](swap): <span class="warn">TODO!</span>

```
sudo swapoff -a
sudo swapon -a
```

[установить разрешения на каталоги и файлы](chmod_chown_r): <span class="warn">TODO!</span>

```
find ./catalog -type d -exec chmod 755 {} \;
find ./catalog -type f -exec chmod 644 {} \;
```

[Создать и разархивировать tgz-архив](tar): <span class="warn">TODO!</span>

```
tar -czf pages.tgz ./pages
tar -xzf pages.tgz
```

Несколько способов создать текстовый файл (пустой, с пустой строкой, с текстом):

```
touch filename.ext
echo > filename.ext
echo "Some text" > filename.ext
```

Варианты создать текстовый файл с определенным текстом:

```
cat > filename.ext"

Some text
```

<kbd>Ctrl</kbd> + <kbd>D</kbd> - для сохранения и завершения редактирования.

    nano filename.ext

<kbd>Ctrl</kbd> + <kbd>O</kbd>, <kbd>Enter</kbd> - сохранить,
<kbd>Ctrl</kbd> + <kbd>X</kbd> - выйти из редактора


{% include_relative dirs_n_files.md %}
