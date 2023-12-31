# Работа с Git-Bash

## Основные команды

### Навигация

**cd** need-dir - Переход в папку need-dir

**cd** need-dir/wpfWork - Переход в папку wpfWork которая находится в папке need-dir

**cd /** - Переход в корневую папку

**cd ..** - Переход в папку на уровень выше (Родительскую)

**cd ~** - Переход в домашнюю папку (User/Username)

**pwd** - Отображает текущее местонахождение

**ls** - Отображает содержимое папки в которой мы находимся

**ls -а** - Отображает все содержимое папки в которой мы находимся (даже скрытые файлы)


### Работа с файлами

#### Создание

**mkdir** new-dir - Создание директории

**touch** new-file.txt - Создание файла

**touch** new-file.txt new-file2.cvs - Создание файлов

#### Удаление

**rmdir** new-dir - Удаление папки new-dir

**rm** new-file.txt - Удаление файла new-file.txt

**rm -r** new-dir2 - Удаление папки new-dir2 и ее содержимого

#### Чтение

**cat** new-file.txt - Вывод содержимого файла new-file.txt

#### Перемещение и копирование

**cp** file.txt ~/new-dir - Копирование файла в другое место

**mv** file.txt ~/new-dir - Перемещение файла или папки в другое место

### Работа с локальным репозиторием

Создаем папку которая будет нашим репозиторием. Переходим в нее через git-bash при помощи команды cd. Используя команду   
**git init** инициализируем в папке репозиторий (чтоб убедиться что все создалось пишем ls -a и видим   
что есть папка с названием .git).

После инициализации файлы внутри папки (если файлов нет то надо создать) надо подготовить к загрузке в репозиторий github.  
Для этого используем команду **git add -all** (либо можно подготовить лишь 1 файл **git add text.txt**). После подготовки надо сохранить эти файлы и 
прописать коммит (коммит это краткое описание внесенных изменений). Для создания коммита надо использовать команду **git commit -m 'Тут кратко пишем изменения'**.  
Для проверки статуса репозитория используют команду **git status**. Для просмотра истории коммитов пишут **git log**.  

### Работа с удаленным репозиторием

После подготовки и сохранения файлов надо отправить (запушить) их в удаленный репозиторий.
Первоначально их надо связать. Переходим в удаленный репозиторий и копируем там ссылку на репизиторий https  
используем команду **git remote add origin https://github.com/ИМЯПОЛЬЗОВАТЕЛЯ/Work-With-Git.git** (ссылку можно вставить нажав ПКМ + Paste).  
Чтобы убедиться что репозитории связанны пришем **git remote -v** и видим 2 строчки.  
Для первой отправки наших коммитов надо использовать команды: 
**git branch -M main**
**git push -u origin main**

### Файл README.md

Данный файл необходим чтоб другие пользователи смогли просмотреть информацию о проекте (кто и зачем создал, какие технологии использовал, о чем проект и тп).   
Этот файл можно создать в ручную в локальном репозитории и при помощи разметки MarkDown заполнить документ в обычном блокноте.
Шпаргалка для изучения данной разметки  [Разметка Markdown]https://www.markdownguide.org/cheat-sheet/

 