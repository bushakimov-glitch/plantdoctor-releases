# PlantDoctor — загрузка

Офлайн AI-диагностика комнатных растений: определение вида (50) и состояния
(20 классов, включая болезни и вредителей) прямо на устройстве.
Фотографии никуда не отправляются — нет серверов, аккаунтов и подписок.

**Языки:** Русский · Қазақша · English
**Android:** 7.0+ (API 24), arm64 / armv7 / x86_64

## Установка (Android)

1. Скачайте файл **PlantDoctor-2.0.0-release.apk** (кнопка *Download* на
   [странице релиза](https://github.com/bushakimov-glitch/plantdoctor-releases/releases)).
2. Откройте скачанный файл. Android попросит разрешить «установку неизвестных
   приложений» для вашего браузера/файлового менеджера — разрешите.
3. Дождитесь установки и запустите приложение.
4. При первом запуске разрешите доступ к камере и уведомлениям
   (напоминания об уходе). Всё остальное работает офлайн.

## Что в 2.0.0 — Умный дом

- **Умный дом (по желанию, локально):** приложение подключается к вашему
  MQTT-брокеру (Mosquitto / Home Assistant / любой локальный) и показывает
  телеметрию датчиков — влажность почвы, температура, влажность воздуха, свет.
  Камера прослеживания (ESP32-CAM) — отдельное устройство: авто-снимки
  растения → офлайн-AI → таймлайн в карточке растения.
- **Демо без железа:** в настройках есть встроенный симулятор датчиков, а
  `tools/demo_node.py` из репозитория поднимает виртуальный узел
  (брокер + датчик + камера) одним Python-процессом.
- **Home Assistant:** узел датчика появляется через MQTT-автообнаружение,
  AI-алерты приложения — на `plantdoctor/alerts/<plantId>`.
- **Важно про сеть:** модуль выключен по умолчанию и общается ТОЛЬКО с
  устройствами в вашей локальной сети (Wi-Fi). В интернете приложение
  не ходит; политики обновлена (раздел «Умный дом и локальная сеть»).
- Подробности по железу: `docs/HARDWARE.md` в репозитории.

### Что было в 2.0.0 без умного дома — 1.2.3

- Исправлена типографика: часть экранов (приветствие, заголовки секций)
  рисовалась моноширинным шрифтом вместо фирменного.
- Исправлены обрезки длинных строк в Настройках и списке видов (Симптомы).
- Всё остальное — без изменений: офлайн-диагностика, 3 языка, база знаний
  с локализацией (ru/kk/en), политика конфиденциальности.

### Что было в 1.2.2

- Локализация базы знаний (уход + лечение) на английский и казахский.
- Оговорка о точности по вредителям + симптомная диагностика.
- Политика конфиденциальности в приложении (ru/kk/en).

## Политика конфиденциальности

<https://bushakimov-glitch.github.io/plantdoctor-privacy/>

## Файлы и контроль

| Файл | Назначение | SHA-256 |
|---|---|---|
| PlantDoctor-2.0.0-release.apk | установка на устройство | 7C8F3E481B2997907A4F74B734C6C49CA67FDEA16FFA5E35AA8784441530A052 |
| PlantDoctor-2.0.0-release.aab | только для Google Play (не для установки) | 3E9BBC4571C7499E9C4E62BB2ABCCDB2A2B72F20014C131160CBBB7B18F8E71C |

Подпись: собственный release-keystore (CN=PlantDoctor, срок действия до 2054) —
обновления будут устанавливаться поверх без переустановки.

---

# PlantDoctor — Түсіру

Үй гүлдерінің офлайн AI-диагностикасы: түрді (50) және күйін (20 класс)
түзелей құрылғыда анықтайды. Суреттер ешқайда жіберілмейді — серверлер,
аккаунттар мен жазылымдар жоқ.

**Тілдер:** Русский · Қазақша · English
**Android:** 7.0+ (API 24), arm64 / armv7 / x86_64

## Орнату (Android)

1. **PlantDoctor-2.0.0-release.apk** файлын жүктеп алыңыз.
2. Файлды ашыңыз. Android «белгісіз қосымшаларды орнатуға» рұқсат сұрайды —
   рұқсат етіңіз.
3. Орнату аяқталғаннан кейін қосымшаны іске қосыңыз.
4. Алғашқы іске қосуда камера мен бағыттауларға рұқсат беріңіз.

## Құпиялылық саясаты

<https://bushakimov-glitch.github.io/plantdoctor-privacy/>

---

# PlantDoctor — Download

Offline AI diagnosis for houseplants: species (50 classes) and condition
(20 classes, incl. diseases and pests) detected directly on your device.
Photos never leave your phone — no servers, accounts or subscriptions.

**Languages:** Русский · Қазақша · English
**Android:** 7.0+ (API 24), arm64 / armv7 / x86_64

## Install (Android)

1. Download **PlantDoctor-2.0.0-release.apk** (*Download* button on the
   [release page](https://github.com/bushakimov-glitch/plantdoctor-releases/releases)).
2. Open the downloaded file. Android will ask to allow "install unknown
   apps" for your browser/file manager — allow it.
3. Wait for the install to finish and launch the app.
4. On first launch, allow camera access and notifications (care reminders).
   Everything else works offline.

## Privacy Policy

<https://bushakimov-glitch.github.io/plantdoctor-privacy/>
