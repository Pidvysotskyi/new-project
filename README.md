Як сторити свій перший репозиторій

Всі операції провоодимо з командного рядка

Створюємо директорію з проектом під назвою "new-project"
cli команда: mkdir new-project

Переходимо до цієї директорії
cli команда: сd new-project

Ініціалізуємо Git в нашій директорії
cli команда: git init

Отримуємо повідомлення
Initialized empty Git repository in <Your working dirrectory>/new-project/.git/

Створюємо у робочій директорії файл "README.md"
cli команда: touch README.md

Перевіряємо чи файл створився
cli команда: ls

Бачимо в середині папки файл с відповідним імям
README.md

Відкриваємо наш проект у редакторі
cli команда: code .

Вносимо зміни до файлу відповідно відкривши його
Я написав лише перший рядок "Як сторити свій перший репозиторій"

Зберігаємо зміни у файлі
Клавіші: Command+S (mac), або Control+S (win)

Додаємо наш файл до відстеження git-ом
cli команда: git add README.md

Робимо коміт наших змін з відповідним повідомленням
cli команда: git commit -m "init"

!! Два попередні кроки можна об`єднати в одну команду: git commit -am "init"

Бачимо відповідне повідомлення про коміт
[main (root-commit) 7b23537] init
1 file changed, 1 insertion(+)
create mode 100644 README.md

Створюємо нову гілку та переходимо в неї
cli команда: git checkout -b development

Отримуємо повідомлення про перехід на новостворену гілку
Switched to a new branch 'development'

Перевіряємо на якій гілці знаходимся
cli команда: git branch

Отримаємо повідомлення з існуючими гілками та активною (з зірочкою)

- development
  main

Відкриваємо нашу гілку проект у редакторі
cli команда: code .

Вносимо зміни до файлу відповідно відкривши його

Робимо коміт наших pмін до активної гілки
cli команда: git commit -am "complete readme file"

Отримуємо повідомлення про успішність коміту
[development 346be3e] complete readme file
1 file changed, 67 insertions(+)

Переходимо до гілки main
cli команда: git checkout main

Отримуємо повідомлення що ми на потрібній гілці
Switched to branch 'main'

Обєднуємо зміни з development до main
cli команда: git merge development

Отримуємо повідомлення про успішний merge
Updating 7b23537..d1cd90e
Fast-forward
README.md | 73 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
1 file changed, 73 insertions(+)

Перевіряємо наш статус
cli команда: git status

Отримуємо повідомлення про те що все закомічено
On branch main
nothing to commit, working tree clean

!! Далі переходимо до свого gitHub аккаунту та сворємо новий репозиторій "new-project"
!! Та копіюємо https адресу нашого репозиторію
!! Повертаємося до командного рядку

Привязуємо свій локальний репозиторій до віддаленого
cli команда: git remote add origin <https адреса віддаленого репозиторію на GitHub>

Перевіряємо чи відбулася привязка
cli команда: git remote -v

Отримуємо повідомлення з шляхами для fetch та push
origin https://github.com/<Your nikName>/new-project.git (fetch)
origin https://github.com/<Your nikName>/new-project.git (push)

Пушимо зміни у віддалений репозиторій
cli команда: git push -u origin main

Отримуємо повідомлення про вдале копіювання файлів
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (9/9), 1.71 KiB | 1.71 MiB/s, done.
Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/Pidvysotskyi/new-project.git

- [new branch] main -> main
  branch 'main' set up to track 'origin/main'.

Готово
