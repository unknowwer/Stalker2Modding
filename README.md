# S.T.A.L.K.E.R. 2 Zone Kit for Codex

Codex-скіл для модингу S.T.A.L.K.E.R. 2, локальний MCP-міст для Windows і вихідний код редакторного адаптера. Flares містить приклад предмета ChemLight з конфігурацією GameData та текстовими експортами Blueprint.

## Встановлення

1. Розпакуй увесь репозиторій і відкрий його кореневу папку в Codex. У Plugins Directory вибери локальне джерело **S.T.A.L.K.E.R. 2 Zone Kit** і встанови **S.T.A.L.K.E.R. 2 Modding**. Визначення локального джерела міститься в `.agents/plugins/marketplace.json`. [Локальні джерела Codex](https://developers.openai.com/plugins/build/plugins)
2. Відкрий GSC Zone Kit. У консолі в режимі **Python** запусти `zonekit_bridge.py` за абсолютним шляхом до скрипту з репозиторію. У режимі **Cmd** введи `py "<абсолютний шлях до zonekit_bridge.py>"`. [Інструкція запуску моста](plugins/stalker2-modding/skills/stalker2-modding/scripts/zonekit-bridge/README.md)
3. У Codex виклич `zonekit_status` і `zonekit_graph_capabilities`. Якщо Zone Kit встановлено в іншому каталозі, задай змінну середовища `STALKER2_ZONE_KIT` і перезапусти Codex.

Плагін запускає вбудований Python Zone Kit. Редактор і MCP-сервер використовують спільну локальну папку `%LOCALAPPDATA%/Stalker2ZoneKitCodex`. Початковий режим читання можна змінити через локальний `bridge_settings.json`.

## Вміст

- [Codex-скіл](plugins/stalker2-modding/skills/stalker2-modding/SKILL.md) охоплює асети, Blueprint, CFG, пакування й перевірку модів.
- [Міст і C++-адаптер](plugins/stalker2-modding/skills/stalker2-modding/scripts/zonekit-bridge/README.md) містять MCP-сервер, запуск редактора, перевірку графів і staged-пакетів. На Zone Kit 5.5.4 перевірено читання вузлів та пінів через T3D. Для запису вузлів і пінів потрібна сумісна збірка нативного адаптера.
- [Flares](examples/Flares/README.md) містить вихідну конфігурацію та знімки трьох робочих Blueprint.
- [Огляд Modding Harness](plugins/stalker2-modding/skills/stalker2-modding/scripts/zonekit-bridge/Modding-Harness-review.md) описує перевірений код пакування, інсталяції й віддаленого доступу.

Якщо завантажуєш ці файли у вебінтерфейсі GitHub, додай вміст розпакованої папки в корінь репозиторію. Збережи прихований каталог `.agents`, щоб Codex знаходив локальне джерело плагіна.
