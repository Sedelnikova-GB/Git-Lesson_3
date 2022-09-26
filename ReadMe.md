# **Инструкция  для работы с Git и удалёнными репозиториями**

## *Что такое Git?*

Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.

> Программа Git берёт на себя контроль версий
проекта и позволяет переключаться между
ними. Обратите внимание: Git хранит не файлы целиком, а отличия между ними. Это позволяет экономить память.
## Подготовка репозитория
Для создание репозитория необходимо выполнить команду *git init*  в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

## *Используется синтаксис языка Markdown*:
* Жирный текст - **
* Курсивный текст - *
* Зачеркнутый текст - ~
* Выделяют заголовки - # в начале строки
* Показать уровень заголовка - подчеркивание знаками = или -
* Нумерованные списки - обозначаются обычными цифрами 1,2,3
* Ненумерованные списки - обозначаются знаками * в начале строки
* Вложенные списки - выполняем отступы

## Создание коммитов

### Git add
Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду *git add* напишите *git add <имя файла>*

### Просмотр состояния репозитория
Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах, или их не было.

### Создание коммитов
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>*. Все файлы для коммита должны быть ***ДОБАВЛЕНЫ*** и сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

## Перемещение между сохранениями
Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с пепозиторием следующим образом: *git checkout <номер коммита>*
>[!Важно]
Для возврата в последнюю сохраненную версию необходимо выполнить команду *git checkout master*.

## Журнал изменений
Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда *git log*. Для этого достаточно выполнить команду *git log* в папке с репозиторием

## Ветки в Git

### Создание ветки

Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*


### Слияние веток

Для того чтобы дабавить ветку в текущую ветку используется команда *git merge <название новой ветки>*.


### Удаление веток
Для удаления ветки ввести команду *git branch -d <название новой ветки>*

### Справочная информация
Для получения справочной информации по ветками используется команда *git branch --help*.

## Работа с удаленными репозиториями.

При запуске команды git init всё происходит только в локальном репозитории: в папке на компьютере пользователя, эту папку создавшего. Но для работы в команде программисты используют удаленные репозитории.

Копировать внешний репозиторий на свой ПК можно командой *git clone*.Команда git clone составная: она не только загружает все изменения, но и пытается слить все ветки на локальном компьютере и в
удаленном репозитории.

*git pull* эта команда позволяет скачать все из текущего репозитория и автоматически сделать merge с нашей версией.

Отправить свою версию репозитория во
внешний репозиторий поможет команда *git
push*. При первом её использовании нужна  авторизация. 
Эта команда позволяет отправить нашу
версию репозитория на внешний
репозиторий. ТРЕБУЕТ АВТОРИЗАЦИИ
на внешнем репозитории.

Команда *pull request*:

*  команда для предложения изменений
* запрос на вливание изменений в репозиторий

В больших компаниях один ответственный за проект создает аккаунт. Другие пользователи дают
команду pull request. Предлагать изменения на GitHub нужно в отдельной ветке. Сначала пользователь копирует репозиторий на свой компьютер, делает fork репозитория, затем
клонирует версию на своём ПК, создаёт ветку с предлагаемыми изменениями, отправляет
изменения командой push в свой аккаунт на GitHub и даёт команду pull request. 

