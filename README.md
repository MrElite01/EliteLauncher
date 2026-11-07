# EliteLauncher

[![Version](https://img.shields.io/github/v/release/MrElite01/EliteLauncher?include_prereleases&label=version&color=e0a000)](https://github.com/MrElite01/EliteLauncher/releases)
[![License](https://img.shields.io/github/license/MrElite01/EliteLauncher?color=22c55e)](https://github.com/MrElite01/EliteLauncher/blob/main/LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows-0078d4)](https://github.com/MrElite01/EliteLauncher/releases)
[![Electron](https://img.shields.io/badge/Electron-45-47848f?logo=electron&logoColor=white)](https://www.electronjs.org/)

**Удобный лаунчер Minecraft с поддержкой скинов Ely.by.**

EliteLauncher — компактный Prism-подобный лаунчер для Windows: установка версий и модлоадеров, Modrinth, несколько сборок в одной версии, умный Drag & Drop и автоматические обновления через GitHub.

> Текущая версия: **0.1.1-beta**

## Возможности

### Умный Drag & Drop
Перетащите `.jar`, `.zip` или целую папку прямо на карточку версии:

- лаунчер сам определяет мод, шейдер, текстурпак или сборку;
- проверяет загрузчик, версию Minecraft, `pack_format` и наличие Iris;
- показывает несовместимые файлы отдельными группами;
- ненужный файл можно убрать значком мусорки и установить всё остальное;
- папки с модами распознаются как сборки и раскладываются по `.minecraft`.

### 6 тем оформления
**Elite**, **Prism Dark**, **Light**, **Coffee**, **Amethyst** и **Minecraft**. Тема применяется мгновенно и сохраняется между запусками.

### Скины Ely.by
Поддержка скинов Ely.by через официальный authlib-патч: скины работают в одиночной игре и на серверах. Патч не затрагивает остальную авторизацию и обновляется автоматически при смене версии authlib.

### Смена сборок
Несколько сборок могут жить в одной версии Minecraft. Лаунчер:

- хранит общие библиотеки между сборками;
- не ломает одну сборку при отключении другой;
- позволяет включать и выключать сборки без переустановки;
- аккуратно удаляет только файлы выбранной сборки.

### Minecraft и модлоадеры
- Vanilla, Fabric, Quilt, Forge и NeoForge;
- список версий загрузчика под выбранную версию Minecraft;
- автоматическая установка Java (Temurin) нужной мажорной версии;
- загрузка клиента, библиотек и ресурсов с проверкой SHA1;
- официальное зеркало Mojang и **BMCLAPI**;
- восстановление повреждённых или отсутствующих файлов при запуске.

### Modrinth
Поиск и установка модов, шейдеров и ресурсов прямо из лаунчера. Проверка совместимости, обязательные зависимости, избранное и закреплённые моды на главном экране.

### Группы и порядок
Создавайте группы, перетаскивайте карточки и целые группы, меняйте ручной порядок — всё сохраняется в конфигурации версии.

### Автообновление
Лаунчер проверяет обновления на GitHub при запуске и раз в 24 часа. Если доступна новая версия, появляется окно с предложением скачать и установить обновление.

## Установка

1. Откройте [Releases](https://github.com/MrElite01/EliteLauncher/releases).
2. Скачайте `EliteLauncher-0.1.1-beta-x64.exe`.
3. Запустите установщик и выберите папку установки.
4. Запустите **EliteLauncher** с рабочего стола или из меню «Пуск».

Установка не требует прав администратора. Лаунчер можно установить и для текущего пользователя.

## Запуск из исходников

Требования: **Node.js 20.19+**, npm.

```bash
npm install
npm run dev
```

Production-сборка:

```bash
npm run build
npm run start
```

Установщик Windows:

```bash
npm run build:win
```

Проверки:

```bash
npm run typecheck
npm run lint
```

## Технологии

- **Electron** + **React 18** + **TypeScript**
- **Tailwind CSS** для интерфейса
- **Zustand** для состояния
- **electron-store** для настроек
- **electron-updater** для автообновлений
- **Modrinth API** для каталога модов
- **BMCLAPI / Mojang** для загрузки Minecraft

## Данные приложения

- Настройки: `%APPDATA%\EliteLauncher\config.json`
- Версии: `%APPDATA%\EliteLauncher\instances`
- Аккаунты: `%APPDATA%\EliteLauncher\accounts.json`
- Скины: `%APPDATA%\EliteLauncher\skins`
- Java: `%APPDATA%\EliteLauncher\java`
- Логи: `%APPDATA%\EliteLauncher\logs\launcher.log`

## Статус

Проект находится в стадии **beta**. Сообщения об ошибках и предложения приветствуются в [Issues](https://github.com/MrElite01/EliteLauncher/issues).

## Лицензия

[MIT](LICENSE)
