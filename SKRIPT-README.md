# Скрипт для скрытия команд / Hide Commands Script

## 🇷🇺 Русский

### Описание
Этот репозиторий содержит Skript-скрипты для скрытия не ванильных (кастомных) команд из Tab автодополнения в Minecraft серверах.

### Что это делает?
- Скрывает команды плагинов из автодополнения Tab
- Оставляет видимыми только ванильные команды Minecraft
- Команды всё ещё можно использовать, но они не появляются при нажатии Tab

### Файлы

#### Скрипты:
- **hide-custom-commands.sk** - Базовая версия (скрывает команды для всех)
- **hide-custom-commands-advanced.sk** - Расширенная версия (с поддержкой пермишенов)

#### Документация:
- **INSTALLATION.md** - Инструкция по установке (English)
- **README-SKRIPT.md** - Подробная документация (Русский)
- **USAGE-EXAMPLES.md** - Примеры использования и FAQ (Русский)

### Быстрый старт
1. Установите плагин Skript на ваш сервер
2. Скопируйте `hide-custom-commands.sk` в `plugins/Skript/scripts/`
3. Выполните `/skript reload hide-custom-commands`
4. Готово!

### Требования
- Minecraft Server (Spigot/Paper/Purpur)
- Skript 2.6 или выше
- Java Edition 1.16+

---

## 🇬🇧 English

### Description
This repository contains Skript scripts to hide non-vanilla (custom/plugin) commands from tab completion in Minecraft servers.

### What does it do?
- Hides plugin commands from tab completion
- Shows only vanilla Minecraft commands
- Commands can still be used, they just won't show in tab completion

### Files

#### Scripts:
- **hide-custom-commands.sk** - Basic version (hides commands for everyone)
- **hide-custom-commands-advanced.sk** - Advanced version (with permission bypass)

#### Documentation:
- **INSTALLATION.md** - Installation guide (English)
- **README-SKRIPT.md** - Detailed documentation (Russian)
- **USAGE-EXAMPLES.md** - Usage examples and FAQ (Russian)

### Quick Start
1. Install Skript plugin on your server
2. Copy `hide-custom-commands.sk` to `plugins/Skript/scripts/`
3. Run `/skript reload hide-custom-commands`
4. Done!

### Requirements
- Minecraft Server (Spigot/Paper/Purpur)
- Skript 2.6 or higher
- Java Edition 1.16+

---

## 📋 Features / Особенности

### Basic Version / Базовая версия
- ✅ Hides all custom commands / Скрывает все кастомные команды
- ✅ Simple and lightweight / Простая и легкая
- ✅ No configuration needed / Не требует настройки
- ✅ Works immediately / Работает сразу

### Advanced Version / Расширенная версия
- ✅ All basic features / Все базовые функции
- ✅ Permission bypass / Обход через пермишены
- ✅ `/toggletab` command / Команда для переключения
- ✅ Admin-friendly / Удобно для администраторов

---

## 🎮 Example / Пример

### Before / До:
```
Player types: /sk[Tab]
Shows: /skript, /skills, /skyblock, /skull, etc.
```

### After / После:
```
Player types: /sk[Tab]
Shows: (nothing - no vanilla commands start with 'sk')

Player types: /ga[Tab]
Shows: /gamemode, /gamerule (only vanilla commands)
```

---

## 🔧 Customization / Настройка

You can edit the vanilla commands list in the script file:
Вы можете редактировать список ванильных команд в файле скрипта:

```yaml
options:
    vanilla-commands: "help", "give", "gamemode", "your-command-here"
```

---

## 📚 Documentation / Документация

- **English**: See [INSTALLATION.md](INSTALLATION.md)
- **Русский**: См. [README-SKRIPT.md](README-SKRIPT.md)
- **Examples/Примеры**: [USAGE-EXAMPLES.md](USAGE-EXAMPLES.md)

---

## 🐛 Troubleshooting / Решение проблем

### Script not working / Скрипт не работает
1. Check Skript version: `/skript info`
2. Reload script: `/skript reload hide-custom-commands`
3. Check errors: `/skript info hide-custom-commands`

### Commands still visible / Команды всё ещё видны
- Check if script is loaded: `/skript list`
- Verify player doesn't have bypass permission
- Reload server or script

---

## 💡 Tips / Советы

- Use basic version for simplicity / Используйте базовую версию для простоты
- Use advanced version for admin control / Используйте расширенную версию для контроля
- Customize the command list for your needs / Настройте список команд под ваши нужды
- Test after installation / Протестируйте после установки

---

## 📄 License / Лицензия

Free to use for any purpose.
Бесплатно для любого использования.

---

## ⭐ Support / Поддержка

If you find this useful, please star the repository!
Если это полезно, пожалуйста, поставьте звезду репозиторию!

---

## 📝 Version / Версия

**v1.0** - Initial release with full documentation
Первый релиз с полной документацией

---

## 🔗 Links / Ссылки

- Skript Plugin: https://github.com/SkriptLang/Skript
- SpigotMC: https://www.spigotmc.org/
- PaperMC: https://papermc.io/

---

Made with ❤️ for Minecraft server administrators
Создано с ❤️ для администраторов Minecraft серверов
