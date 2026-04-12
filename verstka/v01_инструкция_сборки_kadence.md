# v01_инструкция_сборки_kadence.md
## 🎯 Назначение
Пошаговый алгоритм переноса HTML-референса в Kadence Blocks + дочерняя тема.

## 🛠️ 1. Подготовка среды
- Установить `Local WP` или развернуть на хостинге в папке `/dev/`
- Установить тему `Kadence` (бесплатная)
- Установить плагин `Kadence Blocks`
- Создать дочернюю тему: папка `/wp-content/themes/kadence-child/`, внутри `style.css` (см. файл v01_стили_дочерней_темы.css) и пустой `functions.php`
- Активировать дочернюю тему в WP

## 🧱 2. Глобальные настройки Kadence
- Кастомайзер → Colors → Global Colors: `Primary: #0d3b66`, `Accent: #f4a261`, `Background: #f8f9fa`
- Typography: H1-H6 `Manrope`, Body `Roboto Mono`
- Spacing: Global Padding/Margins через настройки темы

## 📐 3. Маппинг блоков (HTML → Kadence)
| HTML-элемент | Kadence Block | Настройки |
|--------------|---------------|-----------|
| `.hero` | Row Layout | Background: Gradient, Padding: 80px 0, Text: white, Container: full width |
| `.grid-3 .card` | Row Layout (3 cols) → Advanced Text / Info Box | Columns gap: 2rem, Mobile: stack, Add custom class `card` |
| `.form-wrap` | Kadence Form | Max width: 640px, Margin: 0 auto, Add class `form-wrap` |
| `.stats` | Row Layout (4 cols) → Advanced Text | Background: #f4a261, Text: #0d3b66, Add class `stats` |

## 📱 4. Мобильная адаптация (правила Kadence)
- В редакторе нажать 📱 → изменить отступы/шрифты только для мобильной точки
- `Row Layout` → Mobile Settings: `Stack Columns`, `Gap: 0.75rem`
- Кнопки: `Min Width: 100%`, `Padding: 16px 0`
- Шрифты в полях: `16px` (чтобы iOS не зумил)
- Скрывать декор через `Visibility → Hide on Mobile`

## ✅ 5. Финальная проверка
- [ ] Все страницы открываются без 404
- [ ] На 📱 текст не обрезается, кнопки кликабельны
- [ ] Кастомные классы (`card`, `form-wrap`, `stats`) подтягивают стили из дочерней темы
- [ ] Скорость > 85 (PageSpeed), изображения в WebP через Optimole
