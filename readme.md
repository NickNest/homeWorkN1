# Команды для работы с консолью

```cd``` перемещение по папкам

```ls``` просмотр содерджимого репозитория

```mkdir``` создание новой папки в текущей директории

```touch``` создание файла в текущей директории 

# Команды для работы с GIT

## Инициализация репозитория

```git init``` (от англ. initialize, «инициализировать») — инициализируй репозиторий.

## Синхронизация локального и удалённого репозиториев  

```git remote add origin https://github.com/YandexPracticum/first-project.git``` (от англ. remote, «удалённый» + add, «добавить») — привяжи локальный репозиторий к удалённому с URL https://github.com/YandexPracticum/first-project.git;

```git remote -v``` (от англ. verbose, «подробный») — проверь, что репозитории действительно связались;

```git push -u origin main``` (от англ. push, «толкать») — в первый раз загрузи все коммиты из локального репозитория в удалённый с названием origin.

💡 ** Ваша ветка может называться master, а не main. Подправьте команду, если это необходимо. **

```git push``` (от англ. push, «толкать») — загрузи коммиты в удалённый репозиторий после того, как он был привязан с помощью флага -u.

## Подготовка файла к коммиту

```git add todo.txt``` (от англ. add, «добавить») — подготовь файл todo.txt к коммиту;

```git add --all``` (от англ. add, «добавить» + all, «всё») — подготовь к коммиту сразу все файлы, в которых были изменения, и все новые файлы;

```git add .``` — подготовь к коммиту текущую папку и все файлы в ней.

## Создание и публикация коммита

```git commit -m "Комментарий к коммиту."``` (от англ. commit, «совершать», фиксировать» + message, «сообщение») — сделай коммит и оставь комментарий, чтобы было проще понять, какие изменения сделаны;

```git push``` (от англ. push, «толкать») — добавь изменения в удалённый репозиторий.

## Просмотр информации о коммитах

```git log``` (от англ. log, «журнал [записей]») — выведи подробную историю коммитов;

```git log --oneline``` (от англ. log, «журнал [записей]» + oneline, «одной строкой») — покажи краткую информацию о коммитах: сокращённый хеш и сообщение.

## Просмотр состояния файлов

```git status``` (от англ. status, «статус», «состояние») — покажи текущее состояние репозитория.

## Добавление изменений в последний коммит

```git commit --amend --no-edit``` (от англ. amend, «исправить») — добавь изменения к последнему коммиту и оставь сообщение прежним;

```git commit --amend -m "Новое сообщение"``` — измени сообщение к последнему коммиту на Новое сообщение.

💡 ** Выйти из редактора Vim: нажать Esc, ввести :qa!, нажать Enter. **

## «Откат» файлов и коммитов

```git restore --staged hello.txt``` (от англ. restore, «восстановить») — переведи файл hello.txt из состояния staged обратно в untracked или modified;

```git restore hello.txt``` — верни файл hello.txt к последней версии, которая была сохранена через git commit или git add;

```git reset --hard b576d89``` (от англ. reset, «сброс», «обнуление» + hard, «суровый») — удали все незакоммиченные изменения из staging и «рабочей зоны» вплоть до указанного коммита.

## Просмотр изменений

```git diff``` (от англ. difference, «отличие», «разница») — покажи изменения в «рабочей зоне», то есть в modified-файлах;

```git diff a9928ab 11bada1``` — выведи разницу между двумя коммитами;

```git diff --staged``` — покажи изменения, которые добавлены в staged-файлах.

# Работа с ветками

## Клонирование чужого репозитория

```git clone git@github.com:YandexPraktikum/first-project.git``` (от англ. clone, «клон», «копия») — склонируй репозиторий с URL first-project.git из аккаунта YandexPraktikum на мой локальный компьютер.

## Создание веток

```git branch feature/the-finest-branch``` (от англ. branch, «ветка») — создай ветку от текущей с названием feature/the-finest-branch;

```git checkout -b feature/the-finest-branch``` — создай ветку feature/the-finest-branch и сразу переключись на неё.

## Навигация по веткам

```git branch``` (от англ. branch, «ветка») — покажи, какие есть ветки в репозитории и в какой из них я нахожусь (текущая ветка будет отмечена символом *);

```git branch -a``` — покажи все известные ветки, как локальные (в локальном репозитории), так и удалённые (в origin, или на GitHub).

```git checkout feature/br``` — переключись на ветку feature/br.

## Сравнение веток

```git diff main HEAD``` (от англ. difference, «отличие», «разница») — покажи разницу между веткой main и указателем на HEAD;

```git diff HEAD~2 HEAD``` — покажи разницу между тем коммитом, который был два коммита назад, и текущим.

## Удаление веток

```git branch -d br-name``` — удали ветку br-name, но только если она является частью main;

```git branch -D br-name``` — удали ветку br-name, даже если она не объединена с main.

## Слияние веток

```git merge main``` (от англ. merge, «сливать», «поглощать») — объедини ветку main с текущей активной веткой. 

## Работа с удалённым репозиторием

```git push -u origin my-branch``` (от англ. push, «толкнуть», «протолкнуть») — отправь новую ветку my-branch в удалённый репозиторий и свяжи локальную ветку с удалённой, чтобы при дополнительных коммитах можно было писать просто git push без -u;

```git push my-branch``` — отправь дополнительные изменения в ветку my-branch, которая уже существует в удалённом репозитории;

```git pull``` (от англ. pull, «вытянуть») — подтяни изменения текущей ветки из удалённого репозитория.
