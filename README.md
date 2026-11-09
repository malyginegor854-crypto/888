# Vivo Bodycam FPS

3D bodycam-style FPS with Vivo ZEISS ultra-zoom camera mode.

Веб-игра на Three.js + обёртка Capacitor для Android APK.

---

## Быстрый старт (игра в браузере)

Открой `www/index.html` в Chrome / Firefox  
или залей папку `www` на любой хостинг (Netlify Drop, GitHub Pages).

После загрузки появится **главное меню** → **Играть**.

---

## Сборка APK через GitHub Actions (без Android Studio)

### 1. Создай репозиторий

1. Зайди на [github.com/new](https://github.com/new)
2. Имя, например: `vivo-bodycam-fps`
3. **Public** (для бесплатных Actions) → Create repository

### 2. Залей этот проект

**С телефона (через браузер):**
1. В репозитории → **Add file → Upload files**
2. Перетащи все файлы из этой папки (не сам zip, а содержимое)
3. Commit

**С ПК:**
```bash
git init
git add .
git commit -m "Initial: Vivo Bodycam FPS"
git branch -M main
git remote add origin https://github.com/ТВОЙ_НИК/vivo-bodycam-fps.git
git push -u origin main
```

### 3. Запусти сборку

1. Вкладка **Actions**
2. Выбери workflow **Build APK**
3. **Run workflow** → Run
4. Подожди 3–6 минут
5. Открой завершённый job → **Artifacts** → скачай `vivo-bodycam-fps-debug`
6. Внутри будет `app-debug.apk` — установи на телефон

> Если Actions не видно: Settings → Actions → General → Allow all actions.

---

## Управление

| Действие | ПК | Телефон |
|----------|----|---------|
| Ходьба | WASD | Джойстик слева |
| Обзор | Мышь (ЛКМ) | Свайп справа |
| Прыжок | Space | Кнопка ПРЫЖОК |
| Взаимодействие | E | Кнопка ДЕЙСТВИЕ |
| Камера VIVO/OPPO | F | Кнопка VIVO |
| Зум | Колесо / кнопки | Слайдер / пилюля / пинч |

Найди в доме телефоны **VIVO** и **OPPO**, возьми в руки и открой камеру — доступен зум до 100× (и выше с насадками).

---

## Структура

```
├── www/                  # веб-игра (HTML + Three.js)
│   ├── index.html
│   ├── manifest.json     # PWA
│   ├── sw.js
│   └── icon-*.png
├── package.json          # Capacitor
├── capacitor.config.json
├── .github/workflows/
│   └── build-apk.yml     # автосборка APK
└── README.md
```

---

## Локальная сборка (если есть Android Studio)

```bash
npm install
npx cap add android
npx cap sync
npx cap open android
```

Build → Build APK(s).

---

## Лицензия

Проект для личного использования. Three.js — MIT.
