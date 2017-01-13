---
layout: post
title:  "Heroku | Продолжение"
date:   2017-01-12 09:59:47 +0200
author: Zhukova
author_linkedin: https://ua.linkedin.com/in/helenzhukova
tags: Heroku
categories: Heroku101
---

# Heroku 101. Продолжение знакомства с сервисом Heroku

Мы, продолжаем проходить инструкцию по настройке приложения NodeJS на облачном сервисе Heroku. 

Первая часть на [Heroku. Первое знакомство](/rest_student/heroku101-first)

  <div class="tabs-panel is-active" id="panel1">
    <div class="responsive-embed widescreen">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/ssNKfiwvv_c?list=PLO33wg5Q-Gf3WejarbKRHmyw-yVX59zIt" frameborder="0" allowfullscreen></iframe>
    </div>
  </div>

### <span class="icon-homecode" id="eight" data-magellan-target="eight"></span> Шаг 8. Посмотреть логи сервера

Знать что происходит на сервере очень важно, чтобы узнать логи сервера есть комманда

```bash
heroku logs --tail
```

которая покажет нам последние сообщения от сервера

![heroku logs](/rest_student/img/heroku-logs.png)

### <span class="icon-homecode" id="nine" data-magellan-target="nine"></span> Шаг 9. Посмотреть в Procfile

Heroku использует специалный файл `Procfile` (это название, расширения нет), для того чтобы запустить указанную вами стартовую комманду для вашего приложения. В случае нашего стартового приложения это комманда

```
web: node index.js
```

![heroku procfile](/rest_student/img/heroku-procfile.png)

### <span class="icon-homecode" id="ten" data-magellan-target="ten"></span> Шаг 10. Установить зависимости

Теперь мы хотим развернуть наше приложение локально, для начла нам надо установить все библиотеки и модули от которых зависит наша программа.  
А сами эти зависимости описаны в файле `package.json`

![heroku package-json](/rest_student/img/heroku-package-json.png)

Чтобы скачать эти модули, выдаем комманду

```bash
npm install
```

![heroku install](/rest_student/img/heroku-install.png)

### <span class="icon-homecode" id="eleven" data-magellan-target="eleven"></span> Шаг 11. Запустить локальный сервер

Теперь мы готовы запустить приложние локально с коммандой 

```
heroku local web
```

![heroku local](/rest_student/img/heroku-local.png)

Теперь мы можем наблюдать наше приложение на локальном серевере по адресу `http://localhost:5000` и оно выглидит аналогично тому, что мы виделе на сервере
 
 
![heroku localhost](/rest_student/img/heroku-localhost.png)

### <span class="icon-homecode" id="twelve" data-magellan-target="twelve"></span> Шаг 12. Внести локальные изменения

### <span class="icon-homecode" id="thirteen" data-magellan-target="thirteen"></span> Шаг 13. Установить addon