# Git

Проект [моего приложения](https://github.com/kazzrom/ConnectingDBToApp.git)

Status: Полезные ресурсы

Этапы сохранений:

modified – index – commit

`git config –global user.name “name”`

`git config –global user.email my_email`

`git init` – создание репозитория

`git add <name_file>` - добавление файла name_file в index

- `-A, --all` - добавление всех файлов в index

`git commit` – сохранение файлов из index’а

- `-m “message”` – сохранение файлов из index’а с сообщением message
- `-a` – сохранение файлов без внесения в index (это те файлы, которые были инициализированы или добавлены в репозиторий)
- `--amend` - изменение последнего коммита
- `--amend -m "New commit message"` - изменение последнего коммита c изменением сообщения

`git status` – показывает статус всех файлов

`git log` – показывает все commit’ы

- `-p` - показывает все commit’ы очень подробно

`git restore <file>` - переводит состояние file, в котором он был на момент последнего commit’а или index’а

`git show <hash>` - показывает подробную информацию о commit’е по его hash’у

- `--staged` - - переводит состояние file, в котором он был на момент последнего commit’а

`git diff` – показывает какие изменения произошли в файлах с последнего commit’а

- `--staged` – показывает какие изменения уже в index’е

`git mv <cur_file> <new_file>` - переименовывает или перемещает cur_file в new_file

`git rm <file>` - удалит file сразу

- --cached – file не удаляется из рабочего каталога, и становится untracked

`git branch <name>` - создание новой ветки name

- `-a` – список всех веток
- `-d <name>` – удаление ветки name

`git checkout <name>` - переключиться на ветку name (указатель HEAD переместился на эту ветку)

- `-b <name>` – создаст ветку name и сразу переместиться на неё
- `-b <name_brunch> <hash>` - создаст name_brunch в commit’е с переданным hash’ем

`git merge <name_brunch>` - объединение ветки name_brunch с текущей веткой, в которой вы находитесь

`git reset`

- `--hard <hash>` - переместить указатели HEAD и ветки, в которой находитесь

`git remote add origin <github_repository>` - добавление удалённого репозитория github_repository и назначение алиаса (имени) origin (это общепринятое имя, оно может быть любым). Теперь к удалённому серверу можно будет обращаться по алиасу origin.

`git remote -v` – показывает подробный вывод репозиториев

`git push origin <name_brunch>` - отправить изменение на сервер origin в ветку name_brunch

- `-f` – отправить свою локальную ветку на удалённый репозиторий

`git clone <url>` -  клонирование репозитория (кода) по url

`git pull origin master` – забирает изменения с удалённого сервера

`git fetch origin` – получить актуальное состояние удалённого репозитория

`git push –set-upstream origin master` – поставит по умолчанию, какую ветку нужно отправлять. После этой установки можно просто вызывать команду `git push`

`git rebase <name_brunch>` - текущую ветку перебазирует с веткой name_brunch, т.е. commit’ы будут последовательны

`git tag <name_tag>` - создание легковесного тега

`git tag -a <name_tag> -m “message”` – супер-тег с сообщением и подробной информацией

`git tag` – вывод всех тегов

`git push <name_tag>` - отправит в репозиторий тег name_tag

`git push –tags` - отправит в репозиторий все теги

### *Памятка:* Как связать локальный и удалённый репозитории

1. git init
2. git add -A
3. git commit -m ‘message’
4. git remote add origin <url_repository>
5. git push origin <name_brunch>

Фактически связывание выполняют только 2 последние команды
