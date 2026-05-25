# CLAUDE.md — Рабочие правила для ops-site

## Что это за проект

Статический сайт-справочник для сотрудников франчайзи АО «Кашалот Шеринг».
Читают дома перед первой сменой и открывают на телефоне прямо на точке.

- **Рабочий URL:** https://tantaklo.github.io/kashalot-staff/
- **Репозиторий:** https://github.com/tantaklo/kashalot-staff
- **Netlify:** ⚠️ заблокирован в РФ — не использовать

## Стек

- Astro 6, output: 'static'
- Тема: astro-theme-pure (cworld1)
- Хостинг: GitHub Pages
- Деплой: `git push` в main → GitHub Actions → сайт обновляется ~1 мин

## Как обновить контент

1. Отредактировать `.md` файл в `src/content/docs/`
2. Запустить из папки проекта:
   ```
   git add .
   git commit -m "update: описание"
   git push
   ```
3. Через ~1 минуту изменения появятся на сайте

## Безопасность

- GitHub логин: `tantaklo`
- Токен: только в `credentials.md` в корне рабочего пространства
- Не коммитить токены, не добавлять их в код

## Что важно не сломать

- `astro.config.ts` — настройки сборки и темы
- `src/content/docs/` — весь контент сайта
- GitHub Actions workflow — деплой

<!-- COURSE-DOCS-START -->
## Project documentation

- `docs/README.md` — карта документации проекта.
- `docs/project-memory.md` — долговечная память проекта: факты, ограничения, словарь и канонические ссылки.
- `docs/bugs-and-gotchas.md` — известные ошибки, gotchas и способы проверки.
- `docs/decision-log.md` — журнал долговечных решений проекта.

Правило: `CLAUDE.md` остается коротким входом в проект. Детали живут в отдельных документах.
<!-- COURSE-DOCS-END -->
