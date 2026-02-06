diff --git a/README.md b/README.md
index fde4f952f9e31303b7b9d9ba57c885884ef78162..567f5805d83fa9945a98ee63dd0791a4dd81c778 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,41 @@
-# Learn_python
\ No newline at end of file
+# Learn_python — Case Battle Tracker Bot
+
+Телеграм-бот для учета операций:
+- ввод средств (пополнение),
+- вывод средств,
+- авто-пересчет баланса и ROI,
+- история операций,
+- сброс своих данных,
+- экспорт общей Excel-базы.
+
+## Что изменено
+- Логика хранения полностью переведена на Excel-файл `case_battle_ledger.xlsx`.
+- В книге два листа:
+  - `Transactions` — все операции;
+  - `Summary` — агрегаты по каждому пользователю (ввод, вывод, итог, ROI).
+- После каждой операции Excel обновляется сразу.
+- Добавлено всплывающее меню (Reply Keyboard) для основных действий.
+
+## Запуск
+1. Установите зависимости:
+   ```bash
+   pip install python-telegram-bot openpyxl
+   ```
+2. Задайте токен:
+   ```bash
+   export BOT_TOKEN="your_bot_token"
+   ```
+3. Запустите:
+   ```bash
+   python start.py
+   ```
+
+## Команды
+- `/start`
+- `/add 1000`
+- `/withdraw 500`
+- `/balance`
+- `/stats`
+- `/history`
+- `/export`
+- `/reset`
