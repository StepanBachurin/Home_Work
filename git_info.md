# Начало работы с git
Указываем гиту автора и почту пользователя:
* git config --global user.name
* git config --global user.email
* git config --global core.editor _(для определеления основного редактора для git(необязательно))_

# Работа с репозиторием и добавление файлов для отслеживания

**git init** - инициализирует локальный репозиторий в текущей папке

**git status** - Показывает информацию о состоянии нашего репозитория

**git add** - Добавляет выбранные файлы для отслеживания.

* **git add** *file_name __.extension__* - добавить файл *file_name* с расширением *extension* для отслеживания
* **git add .** - добавить все файлы в репозитории для ослеживания
# Работа с ветками, коммитами и переходами между ними

**git commit** - фиксирует изменения отслеживаемых файлов

* **git commit -m "comment of commit"** - Вызов (с использованием комментария к фиксации) (перед использованием необходимо дать команду отслеживать файлы "**git add**")


* **git commit -a -m "comment of commit"** - Вызов для фиксации изменений всех файлов в реп


**git log** - Показывает все зафиксированные коммиты
* **git log --graph** - добовляет визуальное отображение веток

**git checkout** - Позволяет перейти к другой версии фйла или к другой ветке

* __git checkout name_branch__ - позволяет перейти к ветке с именем __name_branch__
* __git checkout fce2ab98f0ca8a53a57a7d2c61e5f18c183bf07d__ - к верссии с этим именем после checkout (его можно указывать более сокращенно, например **fce2**)

**git diff** - Показывает все не закомиченные изменения

**git branch**

* __git branch__ - *Показывает все существующие ветки на данный момент*

* __git branch name_branch__ - *добавляет ветку с именем name_branch*

* __git branch -d name_branch__ - Удоляет ветку с именем name_branch (если ветка никуда не влита, то будет ошибка)
. Чтобы избежать ошибки нужно влить эту ветку в другую или заменить "-d" на  "-D"

**git merge** - позволяет влить одну ветку в другую ветку

* **git merge name_merge** - *эта команда вливает ветку name_merge в текущую ветку (в котоой мы находимся в данный момент)*

# Дополнительные функции
**--help** - справка
* Например **git commit --help** - вызов справки для commit

**clear** - очистить консоль

**cd** - change directory
* **cd name_file** - Перейти к фалу name_file в текущей директории
* **cd ..** - выйти на один уровень вверх
* **cd ../..** - выйти на два уровеня вверх

# Работа с удаленным репозиторием
## Со своим репозиторием
1. Создать аккаунт на github.com
2. создать локальный репозиторий
3. "подружить" локальный и удаленный репозиторий github при необходимости
4. отправить **git push** с локального репозиторий в удаленный на github
5. Для того чтобы выкачать актуальное состояние из удаленного репозитория нужна команда *git pull*.
## С репозиторием другого пользователя
1. cделать форк *fork* интересуещего нас репозитория на github
2. сделать со своего скопированного реп в github **git clone** в локальный
3. создаем ветку с предлагаемыми изменениями
4. производим все изменения только в этой ветке (правило хорошего тона)
5. отправляем эти изменения на свой аккаунт github **git push**
6. на github появляется возможность отправить (pull request)