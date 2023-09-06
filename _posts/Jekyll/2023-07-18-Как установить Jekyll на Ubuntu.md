---
layout: post
title:  Install jekyll_in Linux Ubuntu
category: Jekyll
---

## Это руководство существует для этих версий ОС:

    Ubuntu 22.04 (Jammy Jellyfish)
    Ubuntu 18.04 (Bionic Beaver)

## На этой странице:

    Предпосылки
    Начало работы
    Установить Руби
    Создайте новый веб-сайт с помощью Jekyll
    Запустите сервер Jekyll
    Доступ к веб-сайту Jekyll
    Заключение 

Jekyll — это бесплатный генератор статических файлов с открытым исходным кодом, написанный на Ruby. Это простая и легкая в использовании система управления контентом, используемая для создания веб-сайта за считанные минуты. Он берет текст, написанный на вашем любимом языке разметки, и использует макеты для создания статического веб-сайта. Вы можете использовать встроенные функции Jekylls для настройки внешнего вида сайтов, URL-адресов, данных, отображаемых на странице, и многого другого. Он предлагает массу функций, таких как постоянные ссылки, категории, страницы, сообщения, настраиваемые макеты и многое другое.

***В этом руководстве мы покажем вам, как установить Jekyll CMS на Ubuntu 22.04.***

## Предпосылки

    Сервер под управлением Ubuntu 22.04.
    
    На вашем сервере настроен пароль root. 

## Начиная

Перед запуском рекомендуется обновить вашу систему до последней стабильной версии. Вы можете обновить его с помощью следующей команды(root):

- apt update -y

- apt upgrade -y

Как только ваша система будет обновлена, установите другие необходимые зависимости, выполнив следующую команду:

- apt install make build-essential curl git tree -y

После установки всех зависимостей можно переходить к следующему шагу.

## Установить Руби

Jekyll написан на Ruby, поэтому вам нужно будет установить его в своей системе. По умолчанию пакет Ruby включен в стандартный репозиторий Ubuntu.

## Выполните следующую команду, чтобы установить Ruby:

- apt install ruby ruby-dev -y

После завершения установки вам нужно будет указать диспетчеру пакетов Ruby для размещения драгоценных камней в домашней папке нашего пользователя.

## Вы можете сделать это, отредактировав файл ~/.bashrc:

- nano ~/.bashrc

## Добавьте в конец файла следующие строки:

- export GEM_HOME=$HOME/gems

- export PATH=$HOME/gems/bin:$PATH

Сохраните и закройте файл, затем активируйте переменную среды с помощью следующей команды:

source ~/.bashrc

## Затем вы можете установить Jekyll и сборщик с помощью команды gem, как показано ниже:

gem install jekyll bundler

После завершения установки можно переходить к следующему шагу.

## Создайте новый сайт с Jekyll

На данный момент Jekyll установлен в вашей системе. Теперь выполните следующую команду, чтобы создать новый веб-сайт с именем **jekyll.example.com**:


- $ jekyll new jekyll.example.com

## После создания веб-сайта вы должны получить следующий результат:
```
  Bundler: Using jekyll 4.2.2
  Bundler: Fetching jekyll-seo-tag 2.8.0
  Bundler: Fetching jekyll-feed 0.16.0
  Bundler: Installing jekyll-feed 0.16.0
  Bundler: Installing jekyll-seo-tag 2.8.0
  Bundler: Fetching minima 2.5.1
  Bundler: Installing minima 2.5.1
  Bundler: Bundle complete! 7 Gemfile dependencies, 31 gems now installed.
  Bundler: Use `bundle info [gemname]` to see where a bundled gem is installed.Don't run Bundler as root. Bundler can ask for sudo if it is needed, and
  Bundler: installing your bundle as root will break this application for all non-root
  Bundler: users on this machine.
New jekyll site installed in /root/jekyll.example.com. 

```
Затем вы перечисляете все файлы и каталоги, созданные Jekyll, с помощью следующей команды:

- $ tree jekyll.example.com

Вы должны получить следующий результат:
```
jekyll.example.com
??? 404.html
??? about.markdown
??? _config.yml
??? Gemfile
??? Gemfile.lock
??? index.markdown
??? _posts
    ??? 2022-09-25-welcome-to-jekyll.markdown

1 directory, 7 files
```
## Запустите сервер Jekyll

## Сначала перейдите в каталог веб-сайта и добавьте зависимость webrick с помощью следующей команды:

- cd jekyll.example.com

bundle add webrick

## Затем запустите веб-сервер Jekyll, выполнив следующую команду:

- jekyll serve --host=0.0.0.0

## После успешного запуска сервера вы должны получить следующий вывод:
```
Configuration file: /root/jekyll.example.com/_config.yml
            Source: /root/jekyll.example.com
       Destination: /root/jekyll.example.com/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
       Jekyll Feed: Generating feed for posts
                    done in 0.375 seconds.
 Auto-regeneration: enabled for '/root/jekyll.example.com'
    Server address: http://0.0.0.0:4000/
  Server running... press ctrl-c to stop.
```
## Доступ к веб-сайту Джекила

На этом этапе Jekyll запущен и прослушивает порт 4000. 

Теперь откройте веб-браузер и введите URL-адрес **http://your-server-ip:4000**, or localhost:4000

Вы будете перенаправлены на страницу Jekyll по умолчанию

## Заключение

В приведенном выше руководстве вы узнали, как установить Jekyll на Ubuntu 22.04. Теперь вы можете изучить Jekyll и создать свой собственный веб-сайт, используя автоматически сгенерированный контент.

