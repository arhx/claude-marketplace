# Claude Code MCP Tools Marketplace

Маркетплейс специализированных плагинов для Claude Code с поддержкой MCP серверов.

## Решаемая проблема

Вместо загрузки всех MCP серверов глобально (что занимает ~27k контекста), каждый плагин загружает только свой MCP сервер при активации.

## Установка маркетплейса

```bash
/plugin marketplace add arhx/claude-marketplace
```

## Доступные плагины

### 1. browser-tester
Тестирование веб-интерфейсов через chrome-devtools-mcp.

**Установка:**
```bash
/plugin install browser-tester@mcp-tools-marketplace
```

**MCP сервер:** chrome-devtools
**Использование:** Автоматически запускается при активации плагина

### 2. docs-helper
Справка по документации через context7 MCP.

**Установка:**
```bash
/plugin install docs-helper@mcp-tools-marketplace
```

**MCP сервер:** context7
**Требуется:** API ключ Context7

**Инициализация:**
```bash
/context-init
```

### 3. figma-export
Конвертация макетов из Figma в HTML/Tailwind.

**Установка:**
```bash
/plugin install figma-export@mcp-tools-marketplace
```

**MCP сервер:** figma
**Использование:** Автоматически запускается при активации плагина

## Преимущества

- ✅ Экономия контекста - MCP загружаются только при необходимости
- ✅ Модульность - устанавливайте только нужные плагины
- ✅ Специализация - каждый агент оптимизирован под свою задачу
- ✅ Изоляция - конфигурация MCP не загромождает глобальные настройки

## Локальное тестирование

Для тестирования маркетплейса локально:

1. Клонируйте репозиторий
2. Добавьте локальный маркетплейс:
   ```bash
   /plugin marketplace add file:///полный/путь/к/claude-marketplace
   ```
3. Установите нужные плагины:
   ```bash
   /plugin install browser-tester@mcp-tools-marketplace
   ```

## Структура проекта

```
_claude_marketplace/
├── .claude-plugin/
│   └── marketplace.json          # Манифест маркетплейса
├── browser-tester/               # Плагин для тестирования браузера
│   ├── .claude-plugin/
│   │   └── plugin.json
│   ├── agents/
│   │   └── browser-tester.md
│   ├── .mcp.json                 # chrome-devtools MCP
│   └── README.md
├── docs-helper/                  # Плагин для документации
│   ├── .claude-plugin/
│   │   └── plugin.json
│   ├── agents/
│   │   └── docs-helper.md
│   ├── commands/
│   │   └── context-init.md       # Команда инициализации
│   ├── .mcp.json                 # context7 MCP
│   └── README.md
├── figma-export/                 # Плагин для Figma
│   ├── .claude-plugin/
│   │   └── plugin.json
│   ├── agents/
│   │   └── figma-export.md
│   ├── .mcp.json                 # figma MCP
│   └── README.md
└── README.md
```

## Лицензия

MIT
