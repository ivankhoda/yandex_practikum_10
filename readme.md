<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Regular Expressions</title>
    <link rel="stylesheet" href="./style.css">
</head>
<body>
    <header class="header">
        <img class="header__logo" src="https://pictures.s3.yandex.net/frontend-developer/dom_bom/logo.svg" alt="logo">
        <p class="header__logo-sub">Регулярные выражения</p>
    </header>
    <main class="container">
        <div class="cover">
            <div class="cover__image"></div>
            <h1 class="cover__heading">RegExp</h1>
        </div>
        <div class="block">
            <form class="form" name="register" action="http://httpbin.org/post" method="POST">
                <h3>Форма регистрации</h3>
                <fieldset class="form__fieldset">
                    <div class="form__field">
                        <input class="form__input" type="text" name="name" pattern="^[А-ЯЁ][а-яё]*(-[А-ЯЁ][а-яё]*)?$"
                               placeholder="Имя" minlength="2" maxlength="20" required />
                        <span class="form__error">Только кириллица, первая буква заглавная, можно ввести от 2 до 20
                            символов </span>
                    </div>
                    <div class="form__field">
                        <input class="form__input" type="text" name="email" pattern="([\w+\.\-]+)(@)([\w\.]+)" placeholder="E-Mail"
                               required />
                        <span class="form__error">e-mail в формате: students-yandex@yandex.ru</span>
                    </div>
                    <div class="form__field">
                        <input class="form__input" type="text" name="tel" placeholder="Телефон"
                               pattern="^(\+7)?(\()?(\s)?([\d\)])+(\s)?[\d\-]{1,10}$" minlength="1" maxlength="17"
                               required/>
                        <span class="form__error">Недопустимый формат номера</span>
                    </div>
                    <div class="form__field">
                        <input class="form__input" type="text" name="url"
                               pattern="^(?<schema>https?:\/\/)?(?<localhost>([a-z0-9]+:))?(?<ip>(([1-9]?\d|1\d\d|2[0-5][0-5]|2[0-4]\d)\.){3}([1-9]?\d|1\d\d|2[0-5][0-5]|2[0-4]\d){2})?(?<website>([a-z0-9]+\.[a-z]+))?(?<domain2>\.[a-z]{2,3})?(?<port>(:[0-9]{1,5})+)?(?<www>www?\.)?|(?<host>[a-z0-9])?(?<domain>\.[a-z]{2,3})?(?<uri>(?<segment>(\/)[a-z_0-9\.-]{1,})+)(?<last_slash>\/)?(?<last_hash>#)?$" placeholder="Ваш сайт" required/>
                        <span class="form__error">URL в формате: http://mysite.ru</span>
                    </div>
                    <button class="form__button" type="text">Отправить</button>
                </fieldset>
            </form>
        </div>
    </main>
    <script src="script.js"></script>
</body>
</html>
