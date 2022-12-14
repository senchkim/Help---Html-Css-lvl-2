# Список часто задаваемых вопросов от студентов которые обучаются на интенсиве HtmlAcademy [HTML/CSS уровень 2](https://htmlacademy.ru/intensive/adaptive)
В этом репозитории я постараюсь максимально подробно ответить на вопросы которые задают студенты практически на каждом интенсиве.
Вопросы будут как самые простые так и достаточно сложные.<br/>

Ответы находятся в свернутой секции ниже вопросов. Просто нажмите на "Ответ", чтобы развернуть.

---

##### Общая информация по курсу.

- *[Макеты] - на текущий момент всего студенту доступно на выбор 3 макета (Барбершоп - учебный проект, его нельзя выбрать в качестве личного)
- Седона / Мишка / Кэт Энерджи - макеты перечислены от простого к сложному, сложность заключается и затрате по времение так как например в Дейвайсе очень много мелких элементов на которые требуется очень много времени, поэтому подумайте(будет ли у Вас достаточно времени) прежде чем брать тот или иной макет.
- *[Защита личного проекта] - после 5 недель обучения наступает период защиты, найдите ссылку на Регламент в котором будет описаны даты защиты (особое внимание обратите на ДЕДЛАЙН сдачи проекта!), у студента 3 попытки на сдачу проекта, проект проверяет случайный наставник. <br>
- #Важно - в процессе защиты может случиться ситуация что вам нужно внести микро-правку в проект, а наставник не может ее смержить и защита закроется через час или два, то как быть?<br>
Решение есть - в интерфейсе защиты есть кнопка `Найти и принять пулл-реквест` - как она работает? Студент вносит правки в ветке `master` и подает ее в `master` академии и только в этом случае студент сам сможет смержить реквест - это главное условие!

##### Структура проекта.

`source` - это папка в которой вы будете разрабатывать проект, в ней лежат файлы верстки / файлы препроцессора / папки с картинками. <br>
`.editorconfig` - в нем лежат настройки линтера для вашего проекта. Линтер позволяет делать код единообразным для всех студентов. <br>
`.gitattributes` - что это такое можете прочитать вот тут - [gitattributes](https://git-scm.com/book/ru/v2/%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-Git-%D0%90%D1%82%D1%80%D0%B8%D0%B1%D1%83%D1%82%D1%8B-Git) <br>
`.gitignore` - если говорить простыя языком то в этом файле описаны те файлы и папки которые гит не будет комитить и отслеживать и соотвествено они не попадут на гитхаб. <br>
`.stylelintrc` - это настройка линтера по стилям препроцессора. <br>
`Readme.md` - файл с описанием проекта. <br>
`gulpfile.js` - файл с настройками сборки проетка в 3 модуле он приходит готовый, но далее студент будет его модифицировать в разделе Автоматизация. <br>
`package.json` - файл с настроками для проекта(крайне важная штука) - более подробно можно почитать тут [package.json](https://habr.com/ru/company/ruvds/blog/423703/)



---

##### 1. Github.
```
Что использовать для работы с Гитхабом консоль или программу Github Desktop?
```

<details><summary><b>Ответ</b></summary>
#### Ответ

Начиная с этого курса и далее студенту придется работать только с консолью - так как появляются ветки и синхронизации между репозиториями. <br>

Вкратце шаги такие:
1) нужно сгенерировать приватный ключ и вставить его в свой репозиторий.
2) нужно свзять свой репозиторий с репозиторием академии( с тем репозиторием откуда вы делали форк!) - `git remote add academy <название репозитория>`
3) ну и далее создавать ветки от `master` согласно заданию, но есть один нюанс после того как ваш наставник смержит задание нужно делать синхронизацию репозиториев (для этого добавляли репозитори для отслеживания шаг-2)
4) после мержа наставником <br> вам нужно забрать изменения к себе в локальный репозиторий, команда <br> `git pull academy master` <br> затем отправить их к себе в репозиторий, команда <br> `git push origin master` <br> и только после этого создавать следующее ветку иначе будет конфликт и решать его студенту придется!

Вся информация по работе с гитом и по синхронизации будет описана в курсе. Советую перечитать ее много раз.
</details>

---

##### 2. БЭМ.
```
Есть ли способ проеерить ошибки по БЭМ не глазами, а автоматически?
```

<details><summary><b>Ответ</b></summary>
#### Ответ

Есть сервис <br>
[Валидатор БЭМ](https://yoksel.github.io/html-tree/) <br>
Вставляете в него свои файлы верстки и ошибки подсветятся желтым цветом.
</details>

---

##### 3. Препроцессор.
```
Какой препроцессор выбрать часто задают вопрос?
```

<details><summary><b>Ответ</b></summary>
#### Ответ

На курсе 2 препроцессора на выбор Less и Sass и по большому счету нет никакой разницы что вы выберете, работают они одинаково, разница лишь в синтаксисе.<br>
[LESS](https://lesscss.org/) <br>
[SASS](https://sass-lang.com/) <br>

Хотя по опыму могу сказать что большинство берет sass.
</details>

---

##### 4. Подход Mobile-First.
```
Какой подход при написании стилей для адаптивности на курсе?
```

<details><summary><b>Ответ</b></summary>
#### Ответ

На курсе будет использован подход mobile-first, от мобильного к десктопному. <br>
[MOBILE FIRST](https://medium.com/@mrmrs_/mobile-first-css-48bc4cc3f60f) <br>

Соответственно макеты на начальном этапе доступны только для мобильного разрешения, а остальная часть планшетная и десктопная будет закрыта(до 4 модуля).
</details>

---

##### 5. Сборка проекта.
```
Сборка проекта что это такое - слышу часто такой вопрос?
```

<details><summary><b>Ответ</b></summary>
#### Ответ

В 3 модуле - Кексобот пришлет, сборку в зависимости от того какой препроцессор вы выбрали. <br>
Так как на курсе мы используем препроцессор, браузер не понимает что это такое - он понимает лишь обычный CSS, и вот сборка и есть та прослойка которая переделает препроцессор в обычный всм знакомый CSS. <br>
Сборка будет сделана на Gulp - в начальном виде она будет дана и уже настроена, ваша задача проста:
1) в корне проекта открыть консоль и установить зависимости `npm i` - после ввода этой команды у вас появится папка `node_modules` в проекте, не трогайте и не удаляйте ее ни в коем случае.
2) затем набрать команду `npm run start` - и запустится сборка проекта и в результате получится файл `style.css` (но прежде нужно описать код стилей в корневом файле `style.less`/ `style.scss`)

Далее я расскажу более подробно про сборку проекта и про некоторые файлы которые есть в проекте, в частности `package.json` / `.gitignore`
</details>

---

##### 6. Пути до шрифтов и до картинок.
```
Очень часто вижу ошибку при указании пути до изображений и шрифтов?
```

<details><summary><b>Ответ</b></summary>
#### Ответ

В шаге 5, я упомянул что браузер не понимает что такое препроцессор и поэтому пути вида:<br>
`../../img` / `../../fonts` - Они ошибочны <br>
так как нужно указывать пути относительно файла `style.css` <br>

А так этот файл находится `css/style.css` - то и подниматься нужно один раз - <br>
`../img` / `../fonts`<br> 
да ваш редактор может ругаться что путь не верный указан в файлах препроцессора, но можете не обращать внимания на это!

#Внимание - при подключнии в файлах верстки - самих стилей или картинок не нужно указывать путь вместе с папкой `source` <br>
`source/css/style.css` -  зачем? Вы и так уже внутри папки `source` <br>
`css/style.css` - вот так должно быть! <br/>
`img/logo.svg` - вот пример для изображения.
</details>

---

##### 7. Создание файлов препроцессора.
```
Частая ошибка это не верное создание файлов препроцессора.
```

<details><summary><b>Ответ</b></summary>
#### Ответ

В папке препроцессора в зависимости от того что вы выберете будет `sass` / `less` нужно создает еще 2 папки<br>
`blocks` - в ней должны делать файлы для ваших блоков, в задании будет сказано что 1 БЭМ-блок равно 1 файл препроцессора, не переживайте если файлов будет много!<br>
`utils` - здесь будут лежать вспомогательные файлы типа шрифтов/миксинов/цветов/переменных/общих стилей<br>

по итогу должно получиться так 2 папки и файл `style.less` / `style.scss` - в этом файле вы будете подключать файлы сначала из папки `utils` потом из папки `blocks`
</details>

---

##### 8. Линтер проекта.
```
На этом проекте появляется понятие линтера - что это такое?.
```

<details><summary><b>Ответ</b></summary>
#### Ответ

Если зайти в файл `package.json` и там найти блок `scripts` - то мы увидим несколько команд.<br>
На старте проекта нам интересны 2 команды: <br>

1) `npm run start` - эту команду я уже упомянал, она нужна для сборки проекта.
2) `npm run lint` - а вот эта команда нужна для запуска линтера чтобы код у всех студентов на курсе был единообразным, были одинаковые пробелы, отступы и так далее..

Совет такой, сделали задание и перед тем как закомитить код вводите в консоли команду `npm run lint` и он покажет в каком файле, на какой строке - какая ошибка (да она будет на английском языке).
</details>

---

##### 9. Сборка проекта.
```
Сборка проекта что это такое?.
```

<details><summary><b>Ответ</b></summary>
#### Ответ

После блока `Погружение в автоматизацию` - вы измените сборку проекта: <br>

1) `npm run build` - эта команда будет делать сборку вашего проекта.

И здесь есть один маленький нюанс после этой команды появится папка `build` - зайдите в нее и откройте файл `index.html` - и убедитесь что все работает корректно - картинки на месте / нет ошибок в консоли браузера .
</details>
