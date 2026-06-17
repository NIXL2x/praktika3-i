# ПР №9. Лицензирование и open-source compliance

## 1. Выбор лицензии

**Выбранная лицензия:** MIT
**Тип:** разрешительная (permissive)

**Что разрешает:**
- Использовать код в коммерческих проектах
- Модифицировать, копировать, распространять
- Сублицензировать и продавать

**Что требует от пользователей кода:**
- Сохранять уведомление об авторских правах и текст лицензии во всех копиях

**Может ли кто-то продавать ваш код:** Да, но с обязательным указанием авторства и сохранением текста лицензии

---

## 2. Результат licensee detect

**Вывод команды:**
License: MIT
Matched files: LICENSE
LICENSE:
Content hash: 4c2c763d64bbc7ef2e58b0ec6d06d90cee9755c9
Attribution: Copyright (c) 2026 Nikita Vikhrov
Confidence: 100.00%
Matcher: Licensee::Matchers::Exact
License: MIT

**Что означает Match %:** Процент совпадения содержимого файла с эталонным текстом лицензии из базы licensee. 100% означает полное совпадение.

**Откуда GitHub знает какая у репозитория лицензия:**
GitHub анализирует содержимое файлов LICENSE, COPYING или аналогичных в корне репозитория и сравнивает с базой известных лицензий через тот же licensee.

---

## 3. SPDX-заголовки

**Пример заголовка который добавили в файл (README.md):**

<!--
SPDX-FileCopyrightText: 2026 Nikita Vikhrov
SPDX-License-Identifier: MIT
-->

Что означает каждая строка:

SPDX-FileCopyrightText — информация об авторе и годе создания файла
SPDX-License-Identifier — SPDX-идентификатор лицензии, под которой распространяется файл

Результат reuse lint:
text
Used licenses: MIT
Files with copyright information: 1 / 99
Files with license information: 1 / 99
Unfortunately, your project is not compliant with version 3.3 of the REUSE Specification :-(
Не все файлы получили заголовок

## 4. Лицензии зависимостей

## 4. Лицензии зависимостей

**Таблица из pip-licenses:**

| Name | Version | License |
|------|---------|---------|
| Flask | 3.1.3 | BSD-3-Clause |
| Jinja2 | 3.1.6 | BSD License |
| MarkupSafe | 3.0.3 | BSD-3-Clause |
| Werkzeug | 3.1.8 | BSD-3-Clause |
| blinker | 1.9.0 | MIT License |
| certifi | 2026.5.20 | Mozilla Public License 2.0 (MPL 2.0) |
| charset-normalizer | 3.4.7 | MIT |
| click | 8.4.1 | BSD-3-Clause |
| idna | 3.18 | BSD-3-Clause |
| itsdangerous | 2.2.0 | BSD License |
| numpy | 2.4.6 | BSD-3-Clause AND 0BSD AND MIT AND Zlib AND CC0-1.0 |
| requests | 2.34.2 | Apache Software License |
| urllib3 | 2.7.0 | MIT |

**Есть ли GPL/AGPL зависимости:** Нет. Все лицензии разрешительные (BSD, MIT, Apache, MPL).

**Что это означало бы для коммерческого проекта:** Если бы были GPL/AGPL-зависимости, пришлось бы либо открывать исходный код всего продукта, либо заменять зависимости на аналоги с разрешительными лицензиями.

## 5. CI-проверка

Ссылка на запущенный workflow: https://github.com/...
Статус licensee job: Passed
Статус reuse job: Отклонился, из-за того, что не все ф
Что произойдёт если добавить GPL-зависимость: ...

## 6. Анализ совместимости

Сценарий 1 (MIT + GPL в коммерческом): ...
Сценарий 2 (Apache-2.0 + MIT): ...
Сценарий 3 (MIT без указания авторства): ...
Сценарий 4 (AGPL в SaaS): ...
Сценарий 5 (нет LICENSE): ...

## 7. Связь с нормативкой

| Аспект | Статья ГК РФ | Как это реализуется |
|--------|-------------|-------------------|
| Авторское право на ПО | ст. 1259 | ... |
| Защита от копирования | ст. 1270 | ... |
| Использование open-source | ст. 1286 | ... |

## Выводы

(что узнали, что было неожиданным)
```
