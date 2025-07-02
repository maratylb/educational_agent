# КАРТА РЕСУРСОВ - БЫСТРАЯ НАВИГАЦИЯ

---
VERSION: 0.1-claude-light
DEPENDS_ON: [agent_core]
UPDATES: []
USED_BY: [query_patterns для поиска ресурсов]
PURPOSE: Централизованная карта всех доступных ресурсов с приоритетами
PRIORITY: HIGH - критично для быстрого доступа
---

## 🎯 СИСТЕМА ПРИОРИТЕТОВ

**Приоритет 1-5** (1 - высший):
- **1**: Критические, часто используемые, всегда доступные
- **2**: Важные, регулярное использование
- **3**: Стандартные учебные материалы
- **4**: Вспомогательные, редкое использование
- **5**: Опциональные, fallback источники

**Estimated Response Time (ERT)**:
- ⚡ Instant (<0.5s) - в памяти/кеше
- 🚀 Fast (0.5-2s) - Project Knowledge
- 🔄 Normal (2-5s) - внешние интеграции
- 🐌 Slow (5s+) - сложные поиски

---

## 📁 CORE SYSTEM FILES

### 🔴 Priority 1 - Critical Navigation
| Ресурс | Путь | ERT | Назначение |
|--------|------|-----|------------|
| Ядро агента | `/core/agent_core.md` | ⚡ | Роль, правила, ограничения |
| Паттерны | `/core/query_patterns.md` | ⚡ | Все типы запросов |
| Эта карта | `/core/resource_map.md` | ⚡ | Навигация |

### 🟠 Priority 2 - System Functions
| Ресурс | Путь | ERT | Назначение |
|--------|------|-----|------------|
| Прогресс | `/system/progress_tracker.md` | 🚀 | Отслеживание состояния |
| Решение проблем | `/system/problem_solver.md` | 🚀 | Fallback стратегии |
| Современный контекст | `/system/modern_context.md` | 🔄 | Актуальные применения |
| Гайд промптинга | `/system/prompting_guide.md` | 🚀 | Принципы Claude |

---

## 📚 SUBJECT-SPECIFIC RESOURCES

### 🟡 Priority 3 - Primary Content
| Ресурс | Путь | ERT | Назначение |
|--------|------|-----|------------|
| Прогресс | `/system/subject_modules.md` | 🔄 | Универсальные шаблоны |

#### Project Knowledge:
| Ресурс | Источник | ERT | Доступ |
|--------|----------|-----|--------|
| Учебные PDF | `[subject]_chapter_***.[filetype]` | 🚀 | Поиск по номеру/теме |
| Оглавление | `[subject]_сontents.[filetype]` | ⚡ | Структура курса |
| Индекс (если имеется) | `[subject]_index.[filetype]` | 🚀 | Быстрый поиск терминов |

#### Google Drive Integration:
| Ресурс | Источник | ERT | Доступ |
|--------|----------|-----|--------|
| Учебные PDF | `[subject]_chapter_***.doc` | 🚀 | Поиск по номеру/теме |
| Оглавление | `[subject]_сontents.doc` | ⚡ | Структура курса |
| Индекс (если имеется) | `[subject]_index.doc` | 🚀 | Быстрый поиск терминов |

#### GitHub Integration:
| Ресурс | Источник | ERT | Доступ |
|--------|----------|-----|--------|
| Учебные PDF | `[subject]_chapter_***.[filetype]` | 🚀 | Поиск по номеру/теме |
| Оглавление | `[subject]_сontents.[filetype]` | ⚡ | Структура курса |
| Индекс (если имеется) | `[subject]_index.[filetype]` | 🚀 | Быстрый поиск терминов |

### 🟢 Priority 4 - Subject Files (GitHub Integration)
| Модуль | Путь | ERT | Специализация |
|--------|------|-----|---------------|
| Зависимости | `/[subject]/[subject]_dependencies.md` | 🚀 | Связи между темами |
| Справочник | `/[subject]/[subject]_reference.md` | 🚀 | Формулы, определения |
| План изучения | `/[subject]/[subject]_study_guide.md` | 🚀 | Методология |

---

## 🌐 EXTERNAL INTEGRATIONS

### 🔵 Priority 1-3 - Connected Services
| Сервис | Доступ | ERT | Использование |
|--------|--------|-----|---------------|
| Google Drive | Project integration | ⚡/🚀/🔄 | Subject Content/Files |
| GitHub | Project integration | ⚡/🚀/🔄 | Core/System/Subject Content/Files |
| Web Search | `web_search()` | 🐌 | Современный контекст |

### ⚫ Priority 5 - Fallback Sources
| Источник | Когда использовать | ERT |
|----------|-------------------|-----|
| General knowledge | Когда специфичные источники недоступны | ⚡ |
| Web Search | Для современных применений, актуальных данных | 🐌 |
| Примеры из опыта | Когда нужны аналогии для объяснения | ⚡ |
| Альтернативные объяснения | При проблемах понимания | 🚀 |

---

## 🔍 СТРАТЕГИИ ДОСТУПА

### Оптимальные пути поиска:

#### ДЛЯ ОПРЕДЕЛЕНИЙ:
```
1. [subject]_reference.md (Priority 4) → быстрый поиск
2. Основной учебный материал (Priority 3) → если не найдено
3. General knowledge (Priority 5) → fallback
```

#### ДЛЯ НАВИГАЦИИ:
```
1. progress_tracker.md → текущая позиция
2. [subject]_dependencies.md → возможные пути
3. [subject]_study_guide.md → рекомендации
```

#### ДЛЯ ПРОБЛЕМ:
```
1. problem_solver.md → известные решения
2. [subject]_reference.md → уточнение понятий
3. modern_context.md → практические примеры
```

#### ДЛЯ СОВРЕМЕННОГО КОНТЕКСТА:
```
1. modern_context.md → сохраненные применения
2. web_search() → новый поиск
3. GitHub/Drive → пользовательские материалы
```

---

## ⚡ QUICK ACCESS PATTERNS

### 🎯 Most Common Queries:
| Запрос | Прямой путь | Fallback |
|--------|-------------|----------|
| "Выпиши параграф X" | PDF → поиск "параграф X" | reference.md |
| "Что такое Y" | reference.md → термин Y | Учебный PDF |
| "Мой прогресс" | progress_tracker.md | Начальное состояние |
| "Что дальше" | dependencies.md + progress | study_guide.md |
| "Не понимаю Z" | problem_solver.md | Альтернативное объяснение |

### 🚀 Speed Optimization:
1. **Cache-friendly пути**: Приоритет 1-2 файлы часто в кеше
2. **Batch requests**: Собирать связанную информацию за один проход
3. **Early termination**: Останавливаться при первом успешном результате
4. **Parallel fallback**: Готовить fallback параллельно с основным поиском

---

## 📊 RESOURCE AVAILABILITY MATRIX

| Тип контента | Project Knowledge | Context Chat | External | Fallback |
|--------------|------------------|--------------|----------|----------|
| Системные файлы | ✅ Всегда | ✅ Кешируются | ❌ | Memory |
| Учебные PDF | ❌ | ✅ Если загружены | ❌ | Description |
| Пользовательские | ❌ | ⚠️ Если shared | ✅ Drive/GitHub | Request |
| Современный контекст | ✅ Накапливается | ⚠️ Временно | ✅ Web | General |

---

## 🔧 ОБРАБОТКА НЕДОСТУПНОСТИ

### Каскад fallback по приоритетам:
```
Priority 1 недоступен → КРИТИЧЕСКАЯ ОШИБКА (не должно быть)
Priority 2 недоступен → Обходной путь через Priority 3-4
Priority 3 недоступен → Использовать Priority 4 + disclaimer
Priority 4 недоступен → Priority 5 (general fallback)
Priority 5 недоступен → Честное признание + рекомендации
```

### Типовые проблемы доступа:
| Проблема | Индикатор | Решение |
|----------|-----------|---------|
| Файл не в контексте | "Не найдено в Project Knowledge" | Проверить загрузку |
| PDF не читается | Поиск возвращает пустоту | Запросить текстовую версию |
| Интеграция отключена | "Drive не подключен" | Альтернативные источники |
| Лимит поисков | 2 неудачные попытки | Переход на fallback |

---

## 🎨 ВИЗУАЛЬНАЯ КАРТА ПОТОКОВ

```
USER QUERY
    ↓
query_patterns.md [определение типа]
    ↓
resource_map.md [ТЫ ЗДЕСЬ]
    ├─→ Priority 1: Core files (instant)
    ├─→ Priority 2: System files (fast)
    ├─→ Priority 3: Subject content (normal)
    ├─→ Priority 4: Subject files (normal)
    └─→ Priority 5: Fallbacks (varies)
         ↓
    [Target Resource]
         ↓
    RESPONSE
```

---

## 📈 МЕТРИКИ ИСПОЛЬЗОВАНИЯ

Отслеживаем для оптимизации:
- **Hit rate** по приоритетам (target: P1-2 > 80%)
- **Fallback frequency** (target: < 20%)
- **Average path length** (target: < 3 steps)
- **Failed searches** (target: < 10%)

---
*Карта оптимизирована для минимизации времени доступа и максимизации успешности поиска*