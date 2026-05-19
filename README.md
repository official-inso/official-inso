<div align="center">

<img src="./.github/assets/logo.svg" alt="INSO" width="120" />

# INSO

**Делаем облачные продукты. И опенсорс заодно.**

</div>

---

## Кто мы

Мы — **INSO**. Пишем облачные продукты, которые держат нагрузку, и параллельно делаем себе инструменты, без которых работать было бы грустно. Эти инструменты потом выкладываем в опенсорс — заходите, пользуйтесь.

Если нужна разработка под заказ — это к нам тоже, подробнее на [studio.insoweb.ru](https://studio.insoweb.ru).

---

## В личном кабинете

Часть наших продуктов живёт в [lk.insoweb.ru](https://lk.insoweb.ru). Что там есть прямо сейчас:

- **Анализ сайтов** — мониторинг доступности и производительности, проверки по расписанию, отчёты по аномалиям.
- **Сокращатель ссылок** — короткие ссылки с аналитикой кликов и географией заходов.
- **Конструктор квизов** — опросы и формы в духе Typeform, со сбором ответов и аналитикой.

И ещё кое-что — заходите, посмотрите.

---

## ELS — наш аналог Sentry

**ELS** (Event Logs Service) — платформа для сбора событий и ошибок из приложений. По сути — аналог Sentry: подключаете SDK, шлёте логи и ошибки, получаете дашборд с поиском, фильтрами, графиками и AI-подсказками по тому, что у вас сломалось.

SDK совместимы по протоколу и одинаково умеют буферизовать события, ретраить и не падать, если сервер недоступен. Выбирайте под свой стек:

### Языки и бэкенд

- **[els-go](https://github.com/official-inso/els-go)** — нативный Go SDK без зависимостей &nbsp; ![Go](https://img.shields.io/badge/-Go-00ADD8?style=flat-square&logo=go&logoColor=white)
- **[els-java](https://github.com/official-inso/els-java)** — JDK 17+, Spring Boot starter, SLF4J appender &nbsp; ![Java](https://img.shields.io/badge/-Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
- **[els-csharp](https://github.com/official-inso/els-csharp)** — .NET Standard 2.0+, middleware для ASP.NET, провайдер `ILogger` &nbsp; ![.NET](https://img.shields.io/badge/-.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)

### JavaScript — клиент и фронтенд

- **[els-client](https://github.com/official-inso/els-client)** — универсальный TS/JS, работает в браузере и Node, ~3 KB gzip &nbsp; ![TS](https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![npm](https://img.shields.io/npm/v/@inso_web/els-client?style=flat-square&color=CB3837&label=npm)
- **[els-react](https://github.com/official-inso/els-react)** — провайдер, хук `useELS`, `ErrorBoundary` &nbsp; ![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black) ![npm](https://img.shields.io/npm/v/@inso_web/els-react?style=flat-square&color=CB3837&label=npm)
- **[els-vue](https://github.com/official-inso/els-vue)** — плагин и composable для Vue 3, дружит с Nuxt, Vite и Quasar &nbsp; ![Vue](https://img.shields.io/badge/-Vue-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white) ![npm](https://img.shields.io/npm/v/@inso_web/els-vue?style=flat-square&color=CB3837&label=npm)
- **[els-next](https://github.com/official-inso/els-next)** — Next.js, App Router и edge runtime &nbsp; ![Next](https://img.shields.io/badge/-Next.js-000?style=flat-square&logo=nextdotjs&logoColor=white) ![npm](https://img.shields.io/npm/v/@inso_web/els-next?style=flat-square&color=CB3837&label=npm)

### JavaScript — серверные фреймворки

- **[els-express](https://github.com/official-inso/els-express)** — middleware для Express 4/5: логгер запросов + обработчик ошибок &nbsp; ![Express](https://img.shields.io/badge/-Express-000?style=flat-square&logo=express&logoColor=white) ![npm](https://img.shields.io/npm/v/@inso_web/els-express?style=flat-square&color=CB3837&label=npm)
- **[els-nest](https://github.com/official-inso/els-nest)** — `LoggerService` для NestJS, request-scoped через `ClsModule` &nbsp; ![Nest](https://img.shields.io/badge/-NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white) ![npm](https://img.shields.io/npm/v/@inso_web/els-nest?style=flat-square&color=CB3837&label=npm)

### Для AI-агентов

- **[@inso_web/els-mcp](https://www.npmjs.com/package/@inso_web/els-mcp)** — MCP-сервер, который даёт AI-агентам (Claude Code, Cursor и подобным) read-only доступ к логам ELS. Можно искать ошибки, разбирать регрессии и спрашивать «а что там у меня горит» прямо из редактора. Подробности и документация — на [mcp.insoweb.ru/els](https://mcp.insoweb.ru/els), сам эндпоинт — `https://mcp.insoweb.ru/els/mcp` &nbsp; ![MCP](https://img.shields.io/badge/-MCP%20server-7C3AED?style=flat-square) ![npm](https://img.shields.io/npm/v/@inso_web/els-mcp?style=flat-square&color=CB3837&label=npm)

---

## opfs-studio

**[opfs-studio](https://github.com/official-inso/opfs-studio)** — браузерное расширение (Manifest V3) для работы с **Origin Private File System**. Ставится в Chrome, Edge или Firefox; открывается в Side Panel браузера или как отдельная вкладка в DevTools — кому как удобнее.

Что умеет: дерево файлов и папок OPFS, редактор кода на базе Monaco (с подсветкой 20+ языков), превью изображений, видео, аудио и PDF, импорт и экспорт с диска, синхронизация изменений в реальном времени.

Самое забавное: похожего инструмента не существует. Ни в Chrome, ни в Chromium у Google штатной возможности заглянуть в OPFS из браузера не завезли — пришлось делать самим.

![TS](https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/-Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Monaco](https://img.shields.io/badge/-Monaco%20Editor-0078D4?style=flat-square&logo=visualstudiocode&logoColor=white)

---

## Чем пользуемся

![TS](https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Go](https://img.shields.io/badge/-Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Java](https://img.shields.io/badge/-Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![C#](https://img.shields.io/badge/-C%23-512BD4?style=flat-square&logo=csharp&logoColor=white)
![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Vue](https://img.shields.io/badge/-Vue-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![Next](https://img.shields.io/badge/-Next.js-000?style=flat-square&logo=nextdotjs&logoColor=white)
![Nest](https://img.shields.io/badge/-NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![Express](https://img.shields.io/badge/-Express-000?style=flat-square&logo=express&logoColor=white)
![Node](https://img.shields.io/badge/-Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/-Nginx-009639?style=flat-square&logo=nginx&logoColor=white)

---

## Написать нам

- по общим вопросам → **[1@insoweb.ru](mailto:1@insoweb.ru)**
- по партнёрству и продажам → **[sale@insoweb.ru](mailto:sale@insoweb.ru)**
- если что-то сломалось → **[support@insoweb.ru](mailto:support@insoweb.ru)**
- нашли баг или уязвимость → **[dev@insoweb.ru](mailto:dev@insoweb.ru)**
- голосом → **[+7 (995) 48-22-000](tel:+79954822000)**

<sub>© INSO</sub>
