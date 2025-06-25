# Вводная
<!-- 
Beej's Guide to Python book source
vim: ts=4:sw=4:nosi:et:tw=72:spell:nojs
-->


_**Эта книга альфа-качества. О...да, возможны ошибки. Когда Вы
найдёте их, пожалуйста, сбросьте замечание на GitHub, или pull request,
или сообщите мне по электронной почте: [`beej@beej.us`](mailto:beej@beej.us).
Когда количество неточностей будет достаточно мало,
я предложу вам печатную версию киги.**_

Привет всем! Вы когда-нибудь размышляли об обучении программированию?
Раздумывали ли Вы о том, как легко достичь этого на языке Python

Да? Тогда этак книга для Вас. Мы начнем с самых основ и постепенно
перейдем к среднему уровню разработчика и решателя проблем! Python — это
язык, который мы будем использовать, чтобы сделать это.

Но к концу книги вы разовьете техники программирования, которые
_превосходят_ языки. После изучения Python, возможно, попробуйте другой
язык, например JavaScript, Go или Rust. У всех них есть свои особенности
для освоения и изучения.

## Аудитория

Начинающие программисты. Если у Вас есть ограниченный опыт или вообще он
отсутствует, то эта книга предназначена Вам!

Личностные предусловия: быть любознательными, любопытными, уметь решать
головоломки и задачи, быть готовыми брать на себя сложные вызовы.

Технические задатки: быть компьютерным пользователем. Вам известно, что
такое файлы, как перемещать (переименовывать) и удалять их, что такое
подкатологи (папки), установка программного обуспечения (ПО), и как
печтатать.

Вы опытный разработчик, желающий начать работать с Python?
Извините, но это, скорее всего, не та книга, которую вы ищете.
Она будет продвигать Вас слишком медленно.
Просто переходите сразу к [fl[официальной
документации Python|https://docs.python.org/3/]].

## Платформа и инструменты

В этой книге я постарался охватить варианты Mac, Windows и Unix
(представлен дистрибутивом Arch Linux).

Мы рассмотрим установку Python 3 и редактора Visual Studio Code.
(Оба бесплатны.) Если у вас уже есть предпочтение по редактору кода
(Vim, Emacs, Sublime, Atom, PyCharm и т. д.), используйте его.
На эту книгу даётся 100%-й сертификат независимости от текстового редактора!

## Официальная домашняя страница и книги на продажу

Официальное расположение этого документа:

* [`http://beej.us/guide/bgpython/`](http://beej.us/guide/bgpython/)

Там же вы найдете примеры кода.

<!--
Чтобы купить красиво переплетенные печатные экземпляры
(некоторые называют их «книгами»), посетите:

* [`http://beej.us/guide/url/bgpbuy`](http://beej.us/guide/url/bgpbuy)

Я буду признателен за покупку, потому что она поможет мне поддерживать
мой образ жизни, связанный с написанием документов!
-->

## Политика использования электронной почты

Я обычно готов помочь с [ix[email to Beej]] вопросами по электронной почте,
так что не стесняйтесь писать, но я не могу гарантировать ответ.
Я веду довольно занятую жизнь, и бывают моменты, когда я просто не могу
ответить на ваш вопрос. В таких случаях я обычно просто удаляю сообщение.
Ничего личного; у меня просто никогда не будет времени дать вам подробный
ответ, который вам нужен.

Как правило, чем сложнее вопрос, тем меньше вероятность, что я отвечу.
Если вы сможете сузить свой вопрос перед отправкой и обязательно включите любую
относящуюся к делу информацию (например, платформу, компилятор, сообщения об
ошибках, которые вы получаете, и все остальное, что, по вашему мнению, может
помочь мне устранить неполадки), вы с большей вероятностью получите ответ.
Для получения дополнительных инсайтов прочтите документ Эрика Реймонда (ESR),
[fl[Как задавать вопросы умным путем|http://www.catb.org/~esr/faqs/smart-questions.html]].

Если вы не получили ответа, поработайте над этим методом "хака" еще,
попробуйте найти ответ, и если он все еще неуловим, напишите мне снова с
информацией, которую вы нашли, и, надеюсь, ее будет достаточно,
чтобы я мог вам помочь.

Теперь, когда я надоел вам, как писать и не писать мне, я просто
хочу сообщить, что я _полностью_ ценю все похвалы, которые книги-руководства
получили за эти годы. Это настоящий моральный подъем, и мне приятно слышать,
что они используются во благо! `:-)` Спасибо!

## Зеркалирование

[ix[mirroring]] Очень сильно приветствуется, если Вы 
создадите зеркало этого сайта, будь то публичное
или частное. Если вы публично зеркалируете сайт и хотите,
чтобы я разместил на его зеркало ссылку с главной страницы исходного,
скиньте мне письмо по адресу
[`beej@beej.us`](beej@beej.us).

## На заметку переводчикам

[ix[translations]] Если есть желание перевести руководство на другой язык,
напишите мне на [`beej@beej.us`](beej@beej.us) и я установлю ссылку на ваш
перевод с главной страницы. Не стесняйтесь добваить свои имя и контактную
информацию к тексту перевода.

В этом исходном документе на Markdown-разметке
используется кодировка UTF-8.

Пожалуйста, учитывайте лицензионные ограничения в разделе
[Авторские права, распространение и юридические вопросы](#legal) ниже.

Если вы хотите, чтобы я разместил перевод у себя - просто попросите.
Я также помещу ссылку на него, если вы хотите разместить его у себя;
любой из этих вариантов хорош.

## Авторские права, распространение и юридические замечания {#legal}

Руководство Beej по программированию на Python защищено авторским правом
© 2019 Брайан «Beej Jorgensen» Холл.

За исключением исходного кода и переводов, указанных ниже, эта
работа лицензирована в соответствии с лицензией
Creative Commons Attribution - Noncommercial - No Derivative Works 3.0.
Чтобы просмотреть копию этой лицензии, посетите

[`https://creativecommons.org/licenses/by-nc-nd/3.0/`](https://creativecommons.org/licenses/by-nc-nd/3.0/)

или отправьте письмо по адресу:
Creative Commons, 171 Second Street, Suite 300, San Francisco, California,
94105, USA.

Одно конкретное исключение из части «Без производных работ» лицензии
заключается в следующем: это руководство может быть свободно переведено на любой
язык, при условии, что перевод будет точным, и руководство будет
перепечатано полностью. К переводу применяются те же лицензионные ограничения,
что и к оригинальному руководству. Перевод также может включать
имя и контактную информацию переводчика.

Исходный код C, представленный в этом документе, настоящим предоставляется в
общественное достояние и полностью свободен от каких-либо лицензионных
ограничений.

Educators are freely encouraged to recommend or supply copies of this
guide to their students.

Unless otherwise mutually agreed by the parties in writing, the author
offers the work as-is and makes no representations or warranties of any
kind concerning the work, express, implied, statutory or otherwise,
including, without limitation, warranties of title, merchantability,
fitness for a particular purpose, noninfringement, or the absence of
latent or other defects, accuracy, or the presence of absence of errors,
whether or not discoverable.

Except to the extent required by applicable law, in no event will the
author be liable to you on any legal theory for any special, incidental,
consequential, punitive or exemplary damages arising out of the use of
the work, even if the author has been advised of the possibility of such
damages.

Contact [`beej@beej.us`](mailto:beej@beej.us) for more information.


## Dedication

Thanks to everyone who has helped in the past and future with me getting
this guide written. And thank you to all the people who produce the Free
software and packages that I use to make the Guide: GNU, Linux,
Slackware, vim, Python, Inkscape, pandoc, many others. And finally a big
thank-you to the literally thousands of you who have written in with
suggestions for improvements and words of encouragement.

I dedicate this guide to some of my biggest heroes and inspirators in the
world of computers: Donald Knuth, Bruce Schneier, W. Richard Stevens,
and The Woz, my Readership, and the entire Free and Open Source Software
Community.


## Publishing Information

This book is written in Markdown using the vim editor on an Arch Linux
box loaded with GNU tools. The cover "art" and diagrams are produced
with Inkscape. The Markdown is converted to HTML and LaTex/PDF by
Python, Pandoc and XeLaTeX, using Liberation fonts. The toolchain is
composed of 100% Free and Open Source Software.


