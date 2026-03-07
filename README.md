# Архетипічна Когнітивістика — Відмінковий Аналізатор

## Структура проекту

```
/
├── api/
│   └── analyze.js      ← серверний проксі (API-ключ тут, безпечно)
├── public/
│   └── index.html      ← весь фронтенд
├── vercel.json         ← конфігурація Vercel
└── README.md
```

---

## Деплой на Vercel (5 кроків)

### 1. Завантаж на GitHub
- Створи новий репозиторій на github.com
- Завантаж всі файли (зберігаючи структуру папок)

### 2. Підключи до Vercel
- Зайди на vercel.com → "Add New Project"
- Вибери свій GitHub-репозиторій
- Натисни "Deploy" (без змін налаштувань)

### 3. Додай API-ключ
- У Vercel: Settings → Environment Variables
- Додай змінну:
  - **Name:** `ANTHROPIC_API_KEY`
  - **Value:** `sk-ant-...` (твій ключ з console.anthropic.com)
- Натисни Save

### 4. Передеплой
- У Vercel: Deployments → три крапки → "Redeploy"

### 5. Готово
- Vercel дасть тобі посилання виду `https://your-project.vercel.app`

---

## Де взяти API-ключ
1. Зайди на console.anthropic.com
2. API Keys → Create Key
3. Скопіюй (показується лише один раз!)

---

## Безпека
API-ключ зберігається лише в Environment Variables Vercel.
Користувачі його ніколи не бачать.
