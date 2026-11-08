# RPO ECO CPU

Background CPU quotas, profiles, and energy stats for ASUSTOR. Adds an Activity Monitor tab and eco widget. Built & tested on AS6602T / ADM 5.1.4.RM62 / Python 3.12+

📥 **[Скачать / Download APK (v1.6.9)](https://github.com)**

---

## 🇺🇸 About Release 1.6.9 (English)

### FIXES
* **Realtek 8188eu Support:** Fixed an issue where reading `sysfs speed` for Realtek 8188eu (USB 0bda:8179) returned `EINVAL`. A read-only driver query confirmed a 150 Mbps speed on your NAS. Added this alternative Wi-Fi reading method as a fallback when sysfs fails.

### WIDGET HARDWARE REFRESH
* **Refresh Button:** If the model or telemetry is unavailable, a compact "Refresh hardware" button will now appear. It requests a re-detection from the active NAS service. The widget displays the waiting status and final confirmation without opening the main window.
* **Eco Analysis:** This does not toggle the CPU mode or trigger automatic analysis. After refreshing the hardware specs, click "Eco Analysis" manually.
* **Hardware Inventory:** The inventory automatically fetches available drive models, network adapters, USB IDs, and drivers. The system does not estimate power consumption (watts) for unknown hardware. The network coefficient (including Wi-Fi) remains an explicit uncalibrated assumption.

### INSTALLATION
1. Go to **App Central** → **Management** → **Manual Install**.
2. Select `homecloud-cpu_1.6.9_x86-64.apk` and install it over your current version.
3. After installation, hard-refresh the ADM page using **Ctrl+F5**.
4. Re-run **"Eco Analysis"** to build a new baseline.
* *Supported Firmware:* ADM 5.1.4.RM62 / AS66, Python 3.12+.

### DATA PRESERVATION & VERIFICATION
* **Settings Retained:** The energy formula, historical totals, tariffs, profiles, schedule, and CPU limitation scope remain unchanged. Missing periods are not backfilled with fictional data.
* **Tested Scenarios:** Verified exactly three isolated use cases: Wi-Fi speed read/rescan; command authorization with zero CPU changes; widget recovery states in RU/EN without window opening.

---

## 🇷🇺 О выпуске 1.6.9 (Russian)

### ИСПРАВЛЕНИЕ
* **Поддержка Realtek 8188eu:** У Realtek 8188eu (USB 0bda:8179) чтение `sysfs speed` возвращает `EINVAL`. На вашем NAS read-only запрос к драйверу подтвердил скорость 150 Мбит/с. Добавлен этот способ чтения для Wi-Fi, когда sysfs не даёт скорость.

### ОБНОВЛЕНИЕ ОБОРУДОВАНИЯ В ВИДЖЕТЕ
* **Кнопка обновления:** При недоступной модели/телеметрии появляется компактная кнопка «Обновить оборудование» / «Refresh hardware». Она запрашивает повторное обнаружение у работающей службы NAS. Виджет показывает ожидание и подтверждение; основное окно не открывается.
* **Анализ Эко:** Режим CPU не переключается, анализ сам не запускается. После обновления показателей нажмите «Анализ Эко» отдельно.
* **Инвентаризация:** Автоматически получает доступные модели накопителей, сетевых адаптеров, USB ID и драйверы. Для нового неизвестного оборудования система не придумывает ватты. Сетевой коэффициент, в том числе Wi-Fi, по-прежнему является явным некалиброванным допущением, а не измерением адаптера.

### УСТАНОВКА
1. Перейдите в **App Central** → **Управление** → **Установка вручную**.
2. Выберите `homecloud-cpu_1.6.9_x86-64.apk` и обновите поверх установленной версии. Удалять прошлую версию не требуется.
3. После установки обновите страницу ADM с помощью **Ctrl+F5**.
4. Новая база сравнения создаётся повторным **«Анализ Эко»**.
* *Поддерживаемая прошивка:* ADM 5.1.4.RM62 / AS66, Python 3.12+.

### СОХРАНЕНИЕ ДАННЫХ И ПРОВЕРКА
* **Сохранение настроек:** Формула энергии, исторические итоги, тариф, профили, расписание и область ограничения CPU не менялись. Неизвестные периоды не заполняются вымышленной энергией.
* **Протестированные сценарии:** Ровно три сценария: Wi-Fi/пересканирование; авторизация команды и отсутствие изменений CPU/энергии; состояния восстановления виджета на RU/EN, без открытия окна.

