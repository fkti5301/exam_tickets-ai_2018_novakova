# Инструкция

**Клонирование репозитория:**

Чтобы начать заполнять ответы, требуется:

1. Установить клиент Git *(ссылки ниже)*

2. Настроить SSH и подключить к своему аккаунту *(ссылки ниже)*

3. Клонировать к себе данный репозиторий:
   ```
   git clone git@github.com:fkti5301/exam_tickets-ai_2018_novakova.git
   ```


**Создание и заполнение ответа на вопрос:**

1. Создать/заполнить файл X.md со своим вопросом и кинуть его в папочку src/tickets. Если создаёте пустой файл и отправляете его в репозиторий, значит, вы заняли этот вопрос, и можете спокойно его заполнять, будучи уверенными, что никто его не возьмёт. Такой подход должен существенно сократить количество конфликтов при мерджах.

2. Обновить SUMMARY.md, добавив туда ссылку на новый файл в виде строки:
   ```
   * [Вопрос #: текст вопроса](tickets/#.md)
   ```

3. Стянуть изменения:
   ```
   git pull
   ```

4. Закоммитить его:
   ```
   git add -A .
   git commit -m "ticket X: [Название коммита. English only]"
   ```
   Примеры названий коммитов: "ticket 1: Create ticket", "ticket 14: Complete ticket", "ticket 40: Fix typo", "ticket 31: Add more info".

5. И отправить в репозиторий:
   ```
   git push
   ```

PS: Создание своих "девелоперских" веток, в которые вы будете заливать свои изменения, категорически приветствуется. :)


**Немного про картинки:**

Картинки можно делать ссылками, но, так как ссылки в Интернете недолговечны, желательно загружать их в репозиторий в папку src/resources/imgs/ и ссылаться на них локально. Картинки называйте по шаблону t[номер билета]_[номер картинки в билете]. Например, 't15_1.png'.


**Формулы:**
Если кому-то требуются формулы, mdBook поддерживает [MathJax](https://www.mathjax.org/).
Смотрим как пользоваться [тут](https://rust-lang-nursery.github.io/mdBook/format/mathjax.html) и [тут](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference).


**GitBook Editor:**

Мы переехали на mdBook, поэтому скорее всего, через GitBook Editor редактировать вы не сможете.

Для тех, кто собирается использовать приложение. У гитбука есть ограничение на количество пользователей одного репозитория, поэтому, чтобы работать всем вместе, делаем следующее: GitBook Editor -> Open -> [Выбираем папку с репозиторием]

Приложение с точки зрения git-а не очень удобное. Тут полностью пропущена стадия staged. Как только нажимаете кнопочку "Save", происходит коммит. Поэтому, чтобы не засорять репозиторий делайте следующие вещи:

* Сохраняйтесь только когда действительно уверены, что готовы отправить это в репозиторий в виде коммита.

* Отключите в настройках автогенерацию названия Settings -> Git -> Automatically generate commit... -> Off.

Пуш осуществляется нажатием кнопки Publish. На данный момент их редактор не поддерживает SSH, поэтому, если хотите пушить с помощью GUI, настраивайте через HTTPS.


**Для тех, кто хочет сразу смотреть на результаты своей работы:**

1. Скачиваем и устанавливаем mdBook [тут](https://github.com/rust-lang-nursery/mdBook/releases), либо по [инструкции](https://github.com/rust-lang-nursery/mdBook/blob/master/README.md)

2. Поднимаем онлайн-книжку локально:
   ```
   mdbook serve path/to/book
   ```

3. Смотрим в браузере по адресу `localhost:3000`


**Пример заполнения билета:**

* [Исходник](SAMPLE.md)


# Полезные ссылки
**Git:**

* [Клиент Git](https://git-scm.com/download/win)

* [Гайд по Git](https://githowto.com/create_a_project)

* [Маленькая книжка-мануал](https://git-scm.com/book/ru/v1)


**Настройка SSH:**

* [Генерация SSH ключа](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

* [Добавление ключа в аккаунт](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

* [Проверка работоспособности](https://help.github.com/articles/testing-your-ssh-connection/)


**Markdown:**

* [Кратко о синтаксисе](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)

* [Понятно о синтаксисе](http://webdesign.ru.net/article/pravila-oformleniya-fayla-readmemd-na-github.html)


**mdBook:**

* [Доки](https://rust-lang-nursery.github.io/mdBook/index.html)

* [README](https://github.com/rust-lang-nursery/mdBook/blob/master/README.md)

* [Скачать](https://github.com/rust-lang-nursery/mdBook/releases)


**MathJax:**

* [Сайт](https://www.mathjax.org/)

* [MathJax в mdBook](https://rust-lang-nursery.github.io/mdBook/format/mathjax.html)

* [Синтаксис кратко](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference)
