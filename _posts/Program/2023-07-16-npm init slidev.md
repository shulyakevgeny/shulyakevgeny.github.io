---
layout: post
title:  Slidev.npm init slidev
category: Program
---

<u>Создать проект</u>

npm init slidev@latest 

<u>Запустить проект</u>

npm run dev

<u>*или все вместе:*</u>

npm install && npm run dev

<u>*для создания нового проекта slidev с Yarn:*</u>

yarn create slidev

yarn init slidev

<u>Установить playwright-chromium:</u>

npm i -D playwright-chromium

Теперь экспортируйте свои слайды в:

==PDF==

slidev export --with-clicks --timeout 0

==PNG==

slidev export --format png

yarn build; npm build

npm build     (запускать в директории dist/)

slidev build (запускать в директории dist/)

вы можете запустить SPA:

npx vite preview (запускать в директории dist/)

<u>Создание сайта SPA(сайт-одностраничник) на Github</u>

 Для воспроизведения Single-Page Application (SPA)

    Шаги для воспроизведения поведения:

    Создайте новый проект Slidev с npm init slidev

    Подождите, пока проект не будет создан и все dep будут установлены.

    Добавьте во 2-ю строку slides.md следующее: monaco: true

    ---
    monaco: true # по умолчанию "dev"
    ---

    Добавьте кодовый блок, в slides.md котором используется monaco.

    ```js
    const count = ref(1)

    const plusOne = computed(() => count.value + 1)

    console.log(plusOne.value) // 2

    plusOne.value++ // error
    ```
    
    На

    ```js {monaco}

    const count = ref(1)    

    const plusOne = computed(() => count.value + 1)

    console.log(plusOne.value) // 2

    plusOne.value++ // error
    ```
    
     Или, вместо добавления кодового блока, вы можете отредактировать например, чтобы использовать monaco,  изменив строку 129 как ```ts {monaco}

    ```ts {monaco}

    import { ref } from 'vue'

    import { useMouse } from '@vueuse/core'

    const counter = ref(0)
    ```

 <u>Запуск в консоли: </u>
 
 npm run build 

*Сгенерированное приложение будет доступно в разделе dist/* .

Вы можете протестировать сгенерированную сборку с помощью веб-сервера (Apache, NGINX, Caddy ... и т.д.) 

<u>запускать в директории dist/:</u>

slidev build --base /test  

*где test - название репозитория на github,куда будете создавать*

    Отпраляете в репозиторий,в моем случае test, из директории dist/

    директорию assets/ и файл index.html.
    
    Дальше получаете ссылку на сайт.
	
	Проверить index.html in dist/ 
	
![solution.png](/img/solution.png)
