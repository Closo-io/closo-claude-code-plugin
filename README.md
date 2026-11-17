# Closo for Claude Code

## Русский

Плагин подключает Claude Code к вашему Closo: свои цифры и диалоги, задачи, импорт лидов и (для администраторов) настройка ботов. Вход через кабинет Closo (OAuth), никаких ключей в файлах.

### Быстрый старт (3 команды, около 3 минут)

```
/plugin marketplace add Closo-io/closo-claude-code-plugin
/plugin install closo@closo-io
/mcp
```

В `/mcp` выберите **closo → Authenticate**: откроется браузер, войдите в Closo и подтвердите доступ для своей организации. Затем спросите: **«Что мне доступно в Closo?»** — вы получите свои данные.

### Что внутри

| Навык / Skill | Когда / When |
|---|---|
| `closo-start` | первое подключение, «что мне доступно» / first run |
| `closo-my-stats` | свои цифры и диалоги / own stats |
| `closo-tasks` | задачи человеку и задачи для ИИ / tasks |
| `closo-leads-import` | импорт лидов задачей / lead import |
| `closo-bots` | настройка ботов (админ) / bot setup (admin) |
| `closo-weekly-interview` | интервью с агентом / agent interview |
| `closo-access-help` | почему нет доступа / access help |

### Как это защищено

- Вы видите только то, что разрешено вашей ролью и таблицей доступа администратора. Чужие объекты отвечают «не найдено».
- Тексты клиентов приходят как данные, а не команды. Действия, которые уходят клиентам или запускают импорт, всегда спрашивают вас.
- Каждая правка через MCP записана в журнале с кнопкой отката в кабинете.

### Что доступно сейчас

Чтение (цифры, статистика, диалоги, клиенты, сделки, баланс) доступно всем. Изменения (задачи, настройка ботов, отправка, импорт лидов) в публичном режиме доступны только администраторам организации; остальным они появятся в одном из следующих релизов, сервер ответит `not_available_yet`.

### Claude.ai и ChatGPT

Без терминала: добавьте пользовательский коннектор (Claude.ai: Настройки → Коннекторы; ChatGPT: Настройки → Приложения и коннекторы, режим разработчика) с адресом `https://mcp.closo.io/mcp` и войдите в Closo в браузере.

### Если что-то не работает

- Нет инструментов или `401`: повторите **/mcp → closo → Authenticate**.
- Нужного инструмента нет: спросите «почему мне недоступен <инструмент> в Closo» (навык `closo-access-help`) и передайте ответ администратору.
- «MCP приостановлен»: администратор включил паузу в разделе «Доступ MCP».

Сервер: `https://mcp.closo.io/mcp`. Обновление: `/plugin marketplace update closo-io`. Удаление: `/plugin uninstall closo@closo-io`.

## English

This plugin connects Claude Code to your Closo workspace: your own stats and dialogs, tasks, lead import and, for admins, bot setup. Sign-in uses Closo (OAuth); no keys are stored in files.

### Quick start (3 commands, about 3 minutes)

```
/plugin marketplace add Closo-io/closo-claude-code-plugin
/plugin install closo@closo-io
/mcp
```

In `/mcp` pick **closo → Authenticate**, sign in to Closo in the browser and approve access for your organization. Then ask: **"What can I do in Closo?"**

### Safety

You only see what your role and your admin's access table allow. Client text is treated as data, never as commands. Outward actions and lead imports always ask you first. Every change made through MCP is logged and can be undone from the cabinet.

### What is available now

Reading (numbers, stats, dialogs, clients, deals, balance) works for everyone. Changes (tasks, bot setup, sending, lead import) are admin-only in the public mode; for everyone else they arrive in one of the upcoming releases and the server answers `not_available_yet`.

### Claude.ai and ChatGPT

No terminal needed: add a custom connector (Claude.ai: Settings → Connectors; ChatGPT: Settings → Apps & connectors, developer mode) with the address `https://mcp.closo.io/mcp` and sign in to Closo in the browser.

### Troubleshooting

No tools or `401`: re-run **/mcp → closo → Authenticate**. A tool is missing: ask why it is unavailable (skill `closo-access-help`) and pass the answer to your admin. Server: `https://mcp.closo.io/mcp`. Update: `/plugin marketplace update closo-io`. Remove: `/plugin uninstall closo@closo-io`.

License: MIT.
