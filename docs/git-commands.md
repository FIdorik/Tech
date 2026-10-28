# Три коммита для первой практической

Команды выполняются пользователем из D:\Tech. Агент не выполнял git add, commit, push или создание PR. Перед сдачей выполните ручные проверки из checklist.md.

Локальная ветка master пока не содержит коммитов. Первый коммит создаёт основу репозитория; реализация и документация добавляются в отдельной ветке двумя следующими коммитами. Всего — ровно три коммита.

## 1. Основа проекта и исходные материалы

```powershell
git add .gitignore package.json package-lock.json dataset example
git commit -m "chore: add project setup and original practice materials"
```

## 2. Страница и адаптивное оформление

```powershell
git switch -c feat/practice-01
git add index.html css/styles.css data images
git commit -m "feat: implement responsive HTML and CSS course page"
```

В коммит входят семантическая разметка, навигация, шесть карточек и таблица из dataset, изображения, форма с валидацией и адаптивные стили.

## 3. Документация и проверки

```powershell
git add README.md docs
git commit -m "docs: describe launch verification and submission"
```

## Отправка и PR

После выполнения трёх коммитов:

```powershell
git push -u origin master
git push -u origin feat/practice-01
gh pr create --base master --head feat/practice-01 --title "Практическая работа №1: HTML и CSS" --body-file docs/pr-description.md
```

Команда gh требует установленного и авторизованного GitHub CLI. Также можно создать PR в браузере: база master, сравниваемая ветка feat/practice-01. Первый коммит будет в master, два следующих попадут в PR; итоговая история работы содержит три коммита.

Последовательность рассчитана на текущее локальное состояние без коммитов. Если удалённый репозиторий содержит другую историю, сначала согласуйте с ней базовую ветку. Не используйте force push.
