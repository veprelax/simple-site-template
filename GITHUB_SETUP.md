# Інструкції для налаштування GitHub та GitHub Pages

## Крок 1: Створення репозиторію на GitHub

1. Перейдіть на https://github.com/new
2. Заповніть форму:
   - **Repository name**: `simple-site-template` (або інша назва)
   - **Description**: "Адаптивний шаблон сайту з респонсивним дизайном"
   - **Visibility**: Public (для безкоштовного GitHub Pages) або Private
   - **НЕ** додавайте README, .gitignore або ліцензію (вони вже є в проєкті)
3. Натисніть кнопку **"Create repository"**

## Крок 2: Завантаження файлів до GitHub

### Варіант A: Через командний рядок (Git)

Якщо у вас встановлений Git:

```bash
# Перейдіть до папки проєкту
cd "C:\Users\User\Desktop\рб1"

# Ініціалізуйте git репозиторій (якщо ще не зроблено)
git init

# Додайте всі файли
git add .

# Створіть перший коміт
git commit -m "Initial commit: Simple Site Template with responsive design"

# Додайте віддалений репозиторій (замініть YOUR_USERNAME та YOUR_REPO на ваші дані)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git

# Завантажте файли
git branch -M main
git push -u origin main
```

### Варіант B: Через GitHub Desktop

1. Завантажте та встановіть GitHub Desktop: https://desktop.github.com/
2. Відкрийте GitHub Desktop
3. Натисніть "File" → "Add Local Repository"
4. Виберіть папку проєкту: `C:\Users\User\Desktop\рб1`
5. Натисніть "Publish repository"
6. Оберіть назву та опис, натисніть "Publish repository"

### Варіант C: Через веб-інтерфейс GitHub

1. Після створення репозиторію, GitHub покаже інструкції
2. Натисніть "uploading an existing file"
3. Перетягніть всі файли з папки проєкту:
   - `index.html`
   - `styles.css`
   - `script.js`
   - `README.md`
   - `.gitignore`
   - `CHECKLIST.md`
   - `GITHUB_SETUP.md`
   - Папку `images/` з усіма SVG файлами
4. Натисніть "Commit changes"

## Крок 3: Налаштування GitHub Pages

1. Перейдіть до вашого репозиторію на GitHub
2. Натисніть на вкладку **"Settings"** (вгорі репозиторію)
3. У лівому меню знайдіть та натисніть **"Pages"**
4. У розділі **"Source"**:
   - Оберіть **"Deploy from a branch"**
   - У полі **"Branch"** оберіть **"main"**
   - У полі **"Folder"** оберіть **"/ (root)"**
5. Натисніть кнопку **"Save"**

## Крок 4: Очікування розгортання

- GitHub автоматично розгорне ваш сайт
- За кілька хвилин (зазвичай 1-2 хвилини) ваш сайт буде доступний
- Ви побачите повідомлення про успішне розгортання на сторінці Settings → Pages

## Крок 5: Отримання посилань

Після успішного розгортання ви отримаєте два посилання:

### Посилання на репозиторій:
```
https://github.com/YOUR_USERNAME/YOUR_REPO
```
(Замініть YOUR_USERNAME та YOUR_REPO на ваші дані)

### Посилання на GitHub Pages:
```
https://YOUR_USERNAME.github.io/YOUR_REPO/
```
(Замініть YOUR_USERNAME та YOUR_REPO на ваші дані)

## Перевірка роботи сайту

1. Відкрийте посилання на GitHub Pages у браузері
2. Перевірте, що всі зображення відображаються
3. Протестуйте адаптивність через інструменти розробника (F12)
4. Перевірте роботу меню на мобільних пристроях

## Важливі примітки

- Якщо ви змінили щось у коді, не забудьте зробити commit та push:
  ```bash
  git add .
  git commit -m "Опис змін"
  git push
  ```
- GitHub Pages автоматично оновлюється після кожного push
- Зміни можуть з'явитися через 1-2 хвилини після push

## Вирішення проблем

### Сайт не відображається
- Перевірте, що файл називається `index.html` (з маленької літери)
- Перевірте, що всі файли завантажені до репозиторію
- Перевірте налаштування GitHub Pages (має бути "main" branch, "/ (root)")

### Зображення не відображаються
- Перевірте, що папка `images/` завантажена до репозиторію
- Перевірте шляхи до зображень у HTML (мають бути `images/about.svg`)

### Стилі не застосовуються
- Перевірте, що файл `styles.css` завантажений
- Перевірте шлях до CSS у HTML: `<link rel="stylesheet" href="styles.css">`

