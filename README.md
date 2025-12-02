# Македонска локализација - Base Translations

[![Odoo Version](https://img.shields.io/badge/Odoo-18.0-blue.svg)](https://www.odoo.com)
[![License: LGPL-3](https://img.shields.io/badge/License-LGPL--3-green.svg)](https://www.gnu.org/licenses/lgpl-3.0)

Директориум со основни македонски преводи за Odoo 18 core модули.

## Содржина

- [Опис](#опис)
- [Структура](#структура)
- [Содржани преводи](#содржани-преводи)
- [Употреба](#употреба)
- [Автор](#автор)

## Опис

Овој директориум содржи PO датотеки со македонски преводи за основните Odoo модули. Ова **НЕ** е стандарден Odoo модул, туку репозиториум за преводи.

> **Забелешка**: За инсталација на преводи, користете ги специфичните локализациски модули како `l10n_mk_product`, `l10n_mk_sale`, `l10n_mk_stock` итн.

## Структура

```
l10n_mk_base/
├── i18n/
│   └── mk_MK.po              # Главен PO фајл со преводи
├── scan_results/             # Резултати од скенирање на преводи
│   ├── ERRORS_html.csv
│   ├── both_placeholder_html.csv
│   ├── html_tags.csv
│   ├── placeholders.csv
│   └── summary.json
├── translation_log.txt       # Лог од процес на превод
├── translation_masking_log.txt
└── README.md
```

## Содржани преводи

### Покриени модули

| Модул | Статус | Покриеност |
|-------|--------|------------|
| base | ✅ | ~95% |
| web | ✅ | ~90% |
| mail | ✅ | ~85% |
| contacts | ✅ | ~95% |
| calendar | ✅ | ~90% |

### Статистика

- **Вкупно стрингови**: ~15,000+
- **Преведени**: ~14,000+
- **Покриеност**: ~93%

## Употреба

### Метод 1: Копирање во Odoo core

```bash
# Копирај PO фајл во соодветен модул
docker cp i18n/mk_MK.po odoo_server:/usr/lib/python3/dist-packages/odoo/addons/base/i18n/mk.po

# Рестартирај Odoo
docker restart odoo_server
```

### Метод 2: Вчитување преку UI

1. Активирај **Developer Mode**
2. **Settings > Translations > Languages**
3. Избери **Macedonian (mk)**
4. Кликни **Update Translation**

### Метод 3: Користи специфични модули

Препорачано е да ги користите специфичните локализациски модули:

- `l10n_mk_product` - Преводи за производи
- `l10n_mk_sale` - Преводи за продажба
- `l10n_mk_stock` - Преводи за залиха
- `l10n_mk_digest` - Преводи за digest

## Scan Results

Директориумот `scan_results/` содржи анализа на квалитет на преводите:

| Датотека | Опис |
|----------|------|
| `ERRORS_html.csv` | Грешки со HTML тагови |
| `placeholders.csv` | Анализа на placeholders |
| `summary.json` | Сумарна статистика |

## Процес на превод

Преводите се генерирани преку:

1. **Извоз од Odoo** - Export на POT датотеки
2. **Машински превод** - Првична верзија
3. **Рачна корекција** - Ревизија на специфични термини
4. **Валидација** - Проверка на placeholders и HTML

### Терминолошки водич

| Англиски | Македонски |
|----------|------------|
| Invoice | Фактура |
| Quotation | Понуда |
| Sales Order | Нарачка за продажба |
| Purchase Order | Нарачка за набавка |
| Warehouse | Магацин |
| Stock | Залиха |
| Lot | Лот |
| Serial Number | Сериски број |

## Ограничувања

- Ова НЕ е инсталабилен Odoo модул
- Преводите треба рачно да се копираат
- Може да има конфликти со официјални Odoo преводи

## Автор

**ЕСКОН-ИНЖЕНЕРИНГ ДООЕЛ Струмица**

- Website: [https://www.eskon.com.mk](https://www.eskon.com.mk)
- Email: info@eskon.com.mk
- GitHub: [https://github.com/Palifra](https://github.com/Palifra)

## Лиценца

Овој материјал е лиценциран под [LGPL-3](https://www.gnu.org/licenses/lgpl-3.0).

## Поврзани модули

- [l10n_mk](https://github.com/Palifra/l10n_mk) - Главен локализациски модул
- [l10n_mk_product](https://github.com/Palifra/l10n_mk_product) - Преводи за производи
- [l10n_mk_sale](https://github.com/Palifra/l10n_mk_sale) - Преводи за продажба
- [l10n_mk_stock](https://github.com/Palifra/l10n_mk_stock) - Преводи за залиха
