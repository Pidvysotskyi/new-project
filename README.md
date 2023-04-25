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

//Два поперtдні кроки можна об`єднати в одну команду: git commit -am "init"

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
