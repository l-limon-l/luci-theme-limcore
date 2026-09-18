# 🎨 luci-theme-limcore

[🇬🇧 English](#-english) | [🇷🇺 Русский](#-русский)

## Preview

| Desktop | Tablet | Phone |
|---------|--------|-------|
| ![Desktop](preview/pc.png) | ![Tablet](preview/tablet.png) | ![Phone](preview/phone.png) |

https://github.com/user-attachments/assets/d3701be2-686f-48ec-b569-c7113755dba5

---

<a id="-english"></a>
## 🇬🇧 English

**luci-theme-limcore** is a clean, modern dark/light theme for OpenWrt LuCI by **l_limon_l**. Based on [luci-theme-aurora](https://github.com/eamonxg/luci-theme-aurora) by eamonxg, with a fully reworked visual layer on top.

### 🚀 Features
- **Warm Neutral Palette**: A proper light and dark mode, not a single palette with inverted colors.
- **Three-Column Docs Layout**: Sidebar, content and a table of contents, so long config pages stay navigable.
- **Frosted Glass Header**: Scroll-aware opacity that keeps the header readable over any content.
- **Floating Toasts**: Notifications appear as floating toasts instead of shifting the page layout.
- **Toggle Checkboxes**: Boolean options are rendered as switches rather than plain checkboxes.
- **Smooth Page Transitions**: Powered by the View Transitions API on browsers that support it.
- **Redesigned Login Page**: A dedicated login screen that matches the rest of the theme.
- **Responsive**: Works on phones and tablets, not only on a desktop browser.

### 📦 Installation

OpenWrt 25.12+ and snapshots use `apk`; earlier versions use `opkg`.

**opkg** (OpenWrt < 25.12):

```sh
cd /tmp && uclient-fetch -O luci-theme-limcore.ipk \
  https://github.com/l-limon-l/luci-theme-limcore/releases/latest/download/luci-theme-limcore_1.0.2-r20260906_all.ipk \
  && opkg install luci-theme-limcore.ipk
```

**apk** (OpenWrt 25.12+):

```sh
cd /tmp && uclient-fetch -O luci-theme-limcore.apk \
  https://github.com/l-limon-l/luci-theme-limcore/releases/latest/download/luci-theme-limcore-1.0.2-r20260906.apk \
  && apk add --allow-untrusted luci-theme-limcore.apk
```

### ✅ Compatibility
- **OpenWrt** 23.05+
- **Chrome/Edge** 111+
- **Safari** 16.4+
- **Firefox** 128+

### 🛠 Development

Built with **Vite 7**, **Tailwind CSS v4** and **pnpm**. See the [Development docs](.dev/docs/DEVELOPMENT.md).

### 📄 License

Apache License 2.0. Credit where it is due: this theme builds on [luci-theme-aurora](https://github.com/eamonxg/luci-theme-aurora) by eamonxg.

### 💬 Contact
- **Telegram**: [t.me/i_limon_i](https://t.me/i_limon_i)

---

<a id="-русский"></a>
## 🇷🇺 Русский

**luci-theme-limcore** — аккуратная современная тема для OpenWrt LuCI со светлым и тёмным режимом, от автора **l_limon_l**. Основана на [luci-theme-aurora](https://github.com/eamonxg/luci-theme-aurora) от eamonxg, визуальный слой переработан полностью.

### 🚀 Возможности
- **Тёплая нейтральная палитра**: Полноценные светлая и тёмная темы, а не одна палитра с инверсией цветов.
- **Трёхколоночная раскладка**: Боковое меню, контент и оглавление — по длинным страницам настроек удобно перемещаться.
- **Шапка с эффектом матового стекла**: Прозрачность меняется при прокрутке, поэтому шапка остаётся читаемой на любом фоне.
- **Всплывающие уведомления**: Тосты появляются поверх страницы и не сдвигают вёрстку.
- **Переключатели вместо галочек**: Логические опции отображаются как тумблеры.
- **Плавные переходы между страницами**: Через View Transitions API в браузерах с поддержкой.
- **Переработанная страница входа**: Отдельный экран авторизации в стиле всей темы.
- **Адаптивность**: Работает на телефонах и планшетах, а не только в десктопном браузере.

### 📦 Установка

OpenWrt 25.12+ и снапшоты используют `apk`, более ранние версии — `opkg`.

**opkg** (OpenWrt < 25.12):

```sh
cd /tmp && uclient-fetch -O luci-theme-limcore.ipk \
  https://github.com/l-limon-l/luci-theme-limcore/releases/latest/download/luci-theme-limcore_1.0.2-r20260906_all.ipk \
  && opkg install luci-theme-limcore.ipk
```

**apk** (OpenWrt 25.12+):

```sh
cd /tmp && uclient-fetch -O luci-theme-limcore.apk \
  https://github.com/l-limon-l/luci-theme-limcore/releases/latest/download/luci-theme-limcore-1.0.2-r20260906.apk \
  && apk add --allow-untrusted luci-theme-limcore.apk
```

### ✅ Совместимость
- **OpenWrt** 23.05+
- **Chrome/Edge** 111+
- **Safari** 16.4+
- **Firefox** 128+

### 🛠 Разработка

Собирается на **Vite 7**, **Tailwind CSS v4** и **pnpm**. Подробности — в [документации для разработчиков](.dev/docs/DEVELOPMENT.md).

### 📄 Лицензия

Apache License 2.0. Тема основана на [luci-theme-aurora](https://github.com/eamonxg/luci-theme-aurora) от eamonxg.

### 💬 Связь
- **Telegram**: [Канал](https://t.me/LimCoreChannel)
