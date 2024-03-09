# Домашнее задание к занятию "`8.01 GIT`" - `Пергунов Дмитрий`

### Задание 1

1. Создали новый репозиторий GIT_HOMEWORK_PERGUNOV
2. Клонировали репозиторий
```bash
terraform@terraform:~$ git clone https://github.com/dimindrol/GIT_HOMEWORK_PERGUNOV
Cloning into 'GIT_HOMEWORK_PERGUNOV'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
```
3. Произвели первоначальную настройку Git
```bash
terraform@terraform:~$ cd GIT_HOMEWORK_PERGUNOV/
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git config --global user.name dimindrol
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git config --global user.email dimindrol_95@mail.ru
```
4. Посмотрели статус
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git status
On branch main
Your branch is up to date with 'origin/main'.
nothing to commit, working tree clean
```
5. Отредактировали файл используя NANO
6. Повторно Выполнили Git STATUS
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git status
On branch main
Your branch is up to date with 'origin/main'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md
no changes added to commit (use "git add" and/or "git commit -a")
```
7. Посмотрели изменения выполнив команды git diff diff --staged
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git diff
diff --git a/README.md b/README.md
index 1678192..9e4d041 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,2 @@
-# GIT_HOMEWORK_PERGUNOV
\ No newline at end of file
+# GIT_HOMEWORK_PERGUNOV
+# Отредактировали файл
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git diff --staged
```
8. Переведили файл в состояние staged
9. Повторно выполнили git diff --staged
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git diff --staged
diff --git a/README.md b/README.md
index 1678192..9e4d041 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,2 @@
-# GIT_HOMEWORK_PERGUNOV
\ No newline at end of file
+# GIT_HOMEWORK_PERGUNOV
+# Отредактировали файл
```
10. Сделали комент и отправили на сервер
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git commit -m 'First commit'
[main 74f3aa4] First commit
 1 file changed, 2 insertions(+), 1 deletion(-)
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 303 bytes | 303.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/dimindrol/GIT_HOMEWORK_PERGUNOV
   7187842..74f3aa4  main -> main
```
11. [Ссылка на Решение (commit)](https://github.com/dimindrol/GIT_HOMEWORK_PERGUNOV/commit/74f3aa4c55b71d9d24161bd15507e12c9ef8e492)

![Название скриншота 2](https://github.com/dimindrol/pergunovdv_8-01-hw/blob/771d0cbfd11b71e3adddc46f03b7e9a6df312337/github.png)`

### Задание 2

1. Создали файл gitignote
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ touch .gitignore
```
2. Добавили правила
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ cat .gitignore 
# ignore all рус
*.рус
cashed/
```
3. Проверили выполнение правил создали файлы внутри папки cashed и файлы которые закачиваются на .рус
И для проверки создали файлы
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ touch chtoto.рус
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ touch kakoito.рус
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ mkdir cashed
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ cd cashed/
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV/cashed$ mkdir newpapka
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV/cashed$ touch file
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV/cashed$ cd newpapka/
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV/cashed/newpapka$ touch file
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV/cashed/newpapka$ cd ..
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV/cashed$ cd ..
```
4. Добавляем нужные нам файлы используя git add и как мы видим файлы на которые мы создали правила добавить в GIT нельзя
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git add .gitignore 
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git add chtoto.рус 
The following paths are ignored by one of your .gitignore files:
chtoto.рус
hint: Use -f if you really want to add them.
hint: Turn this message off by running
hint: "git config advice.addIgnoredFile false"
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git add cashed/
The following paths are ignored by one of your .gitignore files:
cashed
hint: Use -f if you really want to add them.
hint: Turn this message off by running
hint: "git config advice.addIgnoredFile false"
```
5. Делаем комент и пушим
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git commit -m 'ADD .gitignore'
[main 2d4055c] ADD .gitignore
 1 file changed, 3 insertions(+)
 create mode 100644 .gitignore
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git push origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 311 bytes | 311.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/dimindrol/GIT_HOMEWORK_PERGUNOV
74f3aa4..2d4055c  main -> main
```
6. [Ссылка на Решение (commit)](https://github.com/dimindrol/GIT_HOMEWORK_PERGUNOV/commit/2d4055c6ac3c62151a45554584e4868b7dddba69)

![Название скриншота 2](https://github.com/dimindrol/pergunovdv_8-01-hw/blob/a39511463b723e12b721317854c4a04408e22750/gitignore.png)`

### Задание 3

1. Создали новую ветку dev и создали файл test.sh
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git branch dev
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git checkout  dev
Switched to branch 'dev'
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ touch test.sh
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ nano test.sh
```
2. Отредактировали файл test.sh в ветке dev добавили содержимое и запушили
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ nano test.sh
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git add test.sh 
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git commit -m 'Add test.sh'
[dev c891a45] Add test.sh
 1 file changed, 5 insertions(+)
 create mode 100644 test.sh
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git push origin dev
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 393 bytes | 393.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/dimindrol/GIT_HOMEWORK_PERGUNOV/pull/new/dev
remote: 
To https://github.com/dimindrol/GIT_HOMEWORK_PERGUNOV
 * [new branch]      dev -> dev
```
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git diff --staged
diff --git a/test.sh b/test.sh
index 92b33c2..7d17fd6 100644
--- a/test.sh
+++ b/test.sh
@@ -2,4 +2,7 @@
 for var in first "the second" "the third" "I’ll do it"
 do
 echo "This is: $var"
+echo "This is: $var"
+echo "This is: $var"
+echo "This is: $var"
 done
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git commit -m 'edit test.sh'
[dev 88b4c0e] edit test.sh
 1 file changed, 3 insertions(+)
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 337 bytes | 337.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/dimindrol/GIT_HOMEWORK_PERGUNOV
   c891a45..88b4c0e  dev -> dev
3. Добавили в ветку main файл main.sh и запушили
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ touch main.sh
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ nano main.sh 
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git add main.sh 
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git commit -m 'add main sh'
[main e8c34ed] add main sh
 1 file changed, 1 insertion(+)
 create mode 100644 main.sh
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git push origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 315 bytes | 315.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/dimindrol/GIT_HOMEWORK_PERGUNOV
   2d4055c..e8c34ed  main -> main
```
4. Выполнили объединение веток git merge dev
```bash
terraform@terraform:~/GIT_HOMEWORK_PERGUNOV$ git merge dev
Merge made by the 'ort' strategy.
 test.sh | 8 ++++++++
 1 file changed, 8 insertions(+)
 create mode 100644 test.sh
```
5. [Ссылка на Решение (Граф)](https://github.com/dimindrol/GIT_HOMEWORK_PERGUNOV/network)
![Название скриншота 2](https://github.com/dimindrol/pergunovdv_8-01-hw/blob/622134205e319713549fac9f73cee3050329b799/merge.png)`
