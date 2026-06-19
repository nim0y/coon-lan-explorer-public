# 🦝 CoonLanExplorer

**Your personal bridge between devices on the local network / Ваш личный мост между устройствами в локальной сети.**

CoonLanExplorer is a cross-platform file manager and sharing utility that allows you to manage files on a computer directly from a mobile device or another PC within the same local network. Data is transferred directly between devices without utilizing external cloud servers.

CoonLanExplorer — это кроссплатформенный файловый менеджер и инструмент для обмена данными, позволяющий управлять файлами на компьютере напрямую с мобильного устройства или другого ПК в пределах одной локальной сети. Данные передаются напрямую между устройствами без использования внешних серверов или облачных хранилищ.

---

## 🗺 Navigation / Навигация

*   [English Version](#english-readme)
*   [Русская версия](#русская-версия)

---

<a name="english-readme"></a>

# English README

## 📸 Screenshots

<p align="center">
  <img src="screenshots/Screenshot 2026-06-02 222705.png" width="400" alt="Desktop Interface">
  <img src="screenshots/Screenshot 2026-06-02 222724.png" width="400" alt="Desktop Interface">
  <img src="screenshots/Screenshot 2026-06-02 222811.png" width="400" alt="Desktop Interface">
  <img src="screenshots/Screenshot 2026-06-02 222822.png" width="400" alt="Desktop Interface">
</p>
<p align="center">
  <img src="screenshots/Screenshot 2026-06-02 222848.png" width="180" alt="Mobile Explorer 1">
  <img src="screenshots/Screenshot 2026-06-02 222900.png" width="180" alt="Mobile Explorer 2">
  <img src="screenshots/Screenshot 2026-06-02 222911.png" width="180" alt="Mobile Explorer 3">
  <img src="screenshots/Screenshot 2026-06-02 222921.png" width="180" alt="Mobile Explorer">
  <img src="screenshots/Screenshot 2026-06-02 222931.png" width="180" alt="Mobile Explorer">
  <img src="screenshots/Screenshot 2026-06-02 222939.png" width="180" alt="Mobile Explorer">
</p>
<p align="center">
  <i>Desktop and Android Interfaces</i>
</p>

---

## ✨ Features

*   **⚡ Instant Connection:** Scan a QR code displayed on the desktop screen with your mobile device to establish access to the allowed file system directories.
*   **🛡️ Cryptographic Security:** End-to-end encrypted (E2EE) session setup using ECDH (P-256) and AES-256-GCM, authenticated with a mandatory user-defined PIN.
*   **🔍 Network Discovery:** Automatically discover running servers within your local Wi-Fi or LAN subnet using mDNS/NSD.
*   **📦 Smart Downloads:** Download individual files or entire directories, which are automatically packaged as ZIP archives on the fly.
*   **🖥️ Remote Execution:** Open files or launch associated applications on the host server directly from your mobile client.
*   **🚀 Comprehensive Control:** Monitor connected clients, manage active sessions, and configure shared paths from the user interface or CLI.

---

## 📂 Project Structure

The project is structured as a Kotlin Multiplatform repository:

*   **`:androidApp`**: Android application built using Jetpack Compose.
*   **`:desktopApp`**: Desktop application (JVM) built using Compose Multiplatform.
*   **`:server`**: Standalone backend application powered by Ktor.
*   **`:shared`**: Common platform-agnostic business logic, repositories, and UI ViewModels.
*   **`:statistics`**: Internal logging, analytics, and performance measurement module.

---

## 🔒 Security Architecture

*   **Key Agreement:** ECDH (Elliptic Curve Diffie-Hellman P-256) is used for establishing session keys.
*   **Key Derivation:** A mandatory 4-digit PIN is processed as a Pre-Shared Key (PSK) using HKDF-SHA256 to mitigate man-in-the-middle vectors.
*   **Data Encryption:** All payload communication is encrypted using authenticated AES-256-GCM.
*   **Access Isolation:** Built-in path sandboxing prevents file operations outside of designated shared directories.
*   **Token Protection:** Short-lived single-use media tokens are used for streaming and previews, isolating them from primary session tokens.
*   **Hardening:** Server-side rate limiting, session time-to-live (TTL) limits, and automatic IP blocking are implemented.

---

## 🛠 Tech Stack

*   **Kotlin Multiplatform (KMP)** — Shared cross-platform architecture.
*   **Compose Multiplatform** — Unified UI implementation for Desktop and Android.
*   **Ktor (Client & Server)** — Lightweight HTTP and WebSocket network stack.
*   **Koin** — Dependency injection.
*   **Kotlinx Serialization** — Fast, type-safe serialization.
*   **Kotlin Cryptography** — Multiplatform cryptographic operations.

---

## 🚀 Running the Server

You can manage the server via the Desktop/Android graphical user interface, or deploy it on headless environments using the CLI.

### Quick Start (Release Package)
```bash
chmod +x ./server/run-server.sh
./server/run-server.sh --pin 1234 --path ~/Documents
```

### Manual Run (From Source)
```bash
./gradlew :server:run --args="--pin 1234 --path /your/shared/directory"
```

### Interactive CLI Commands
Once active, the server shell accepts the following diagnostic and control commands:

*   `status` — Displays current state, listening port, and active shares.
*   `clients` — Lists connected clients and transfer statistics.
*   `kick <id>` — Forcefully disconnects a specific client session by ID.
*   `ip` — Prints local IP addresses and streaming endpoints.
*   `unban <ip>` — Clears security-related blocks/bans for an IP address.
*   `paths` — Details active shared folders and their states.
*   `qr` — Outputs connection details as a JSON object for manual input.
*   `pin <4-digits>` — Updates the access PIN on the fly.
*   `port <port>` — Rebinds the server to a new port.
*   `add <path>` / `remove <path>` — Modifies active shared paths.
*   `start` / `stop` — Toggles the embedded Ktor engine status.
*   `exit` / `quit` — Gracefully stops active processes and terminates.

> *Note: A 4-digit PIN is strictly required during startup for security purposes.*

---

## 📥 Download

Pre-built binaries can be obtained from the **[Releases](https://github.com/nim0y/coon-lan-explorer-public/releases)** tab.

*   **Linux/Unix (CLI Only):** Download the `.zip` archive from the releases page.
*   **Windows:** Download the `.msi` desktop installer.
*   **Android:** Available on **[RuStore](https://www.rustore.ru/catalog/app/com.coonstudio.coonlanexplorer)**, or as direct `.apk` downloads in Github Releases.

---

## 💬 Feedback & Support

If you encounter an issue or have a feature proposal:
1. Navigate to the **[Issues](https://github.com/nim0y/coon-lan-explorer-public/issues)** section.
2. Search for existing reports to avoid duplicates.
3. Open a new ticket with clear reproduction steps or design proposals.

---

<a name="русская-версия"></a>

# Русская версия

## 📸 Скриншоты

<p align="center">
  <img src="screenshots/Screenshot 2026-06-02 222705.png" width="400" alt="Интерфейс ПК">
  <img src="screenshots/Screenshot 2026-06-02 222724.png" width="400" alt="Интерфейс ПК">
  <img src="screenshots/Screenshot 2026-06-02 222811.png" width="400" alt="Desktop Interface">
  <img src="screenshots/Screenshot 2026-06-02 222822.png" width="400" alt="Desktop Interface">
</p>
<p align="center">
  <img src="screenshots/Screenshot 2026-06-02 222848.png" width="180" alt="Мобильная версия 1">
  <img src="screenshots/Screenshot 2026-06-02 222900.png" width="180" alt="Мобильная версия 2">
  <img src="screenshots/Screenshot 2026-06-02 222911.png" width="180" alt="Мобильная версия 3">
  <img src="screenshots/Screenshot 2026-06-02 222921.png" width="180" alt="Mobile Explorer">
  <img src="screenshots/Screenshot 2026-06-02 222931.png" width="180" alt="Mobile Explorer">
  <img src="screenshots/Screenshot 2026-06-02 222939.png" width="180" alt="Mobile Explorer">
</p>
<p align="center">
  <i>Интерфейс приложения на Desktop и Android</i>
</p>

---

## ✨ Основные возможности

*   **⚡ Мгновенное подключение:** Отсканируйте QR-код на экране монитора мобильным устройством, чтобы получить доступ к разрешенным директориям.
*   **🛡️ Надежное шифрование:** Сквозное шифрование сессии (E2EE) с помощью ECDH (P-256) и AES-256-GCM, защищенное обязательным пользовательским PIN-кодом.
*   **🔍 Сетевое обнаружение:** Автоматический поиск активных серверов в локальной Wi-Fi/LAN сети через протоколы mDNS/NSD.
*   **📦 Умное скачивание:** Загрузка отдельных файлов или директорий, автоматически упаковываемых в ZIP на лету.
*   **🖥️ Удаленные действия:** Открытие файлов или запуск связанных приложений на хост-сервере прямо с мобильного клиента.
*   **🚀 Контроль и мониторинг:** Отслеживание подключенных клиентов, управление сессиями и путями доступа через графический интерфейс или консоль.

---

## 📂 Структура проекта

Репозиторий организован по принципам Kotlin Multiplatform:

*   **`:androidApp`**: Мобильное приложение Android на Jetpack Compose.
*   **`:desktopApp`**: Настольное приложение (JVM) на Compose Multiplatform.
*   **`:server`**: Автономный файловый сервер на базе Ktor.
*   **`:shared`**: Общая бизнес-логика, репозитории данных и UI ViewModels.
*   **`:statistics`**: Платформо-независимый модуль для сбора аналитики и логов.

---

## 🔒 Архитектура безопасности

*   **Согласование ключей:** ECDH (Elliptic Curve Diffie-Hellman P-256) используется для генерации сессионных ключей.
*   **Аутентификация:** Обязательный 4-значный PIN выступает в роли Pre-Shared Key (PSK) при деривации ключей (HKDF-SHA256) для предотвращения атак типа MitM.
*   **Шифрование данных:** Все пакеты данных шифруются по стандарту AES-256-GCM.
*   **Песочница путей:** Механизм path sandboxing исключает выполнение файловых операций за пределами явно разрешенных директорий.
*   **Безопасный медиа-стриминг:** Использование короткоживущих одноразовых токенов для стриминга и превью защищает основные токены авторизации.
*   **Защитные механизмы:** Ограничение частоты запросов (rate limiting), лимит времени жизни сессии (TTL) и автоматическая блокировка подозрительных IP-адресов.

---

## 🛠 Технологический стек

*   **Kotlin Multiplatform (KMP)** — Кроссплатформенная архитектура бизнес-логики.
*   **Compose Multiplatform** — Единый декларативный интерфейс для Android и Desktop.
*   **Ktor (Client & Server)** — Легковесный сетевой стек для HTTP и WebSockets.
*   **Koin** — Внедрение зависимостей (Dependency Injection).
*   **Kotlinx Serialization** — Быстрая сериализация данных.
*   **Kotlin Cryptography** — Мультиплатформенная криптография.

---

## 🚀 Запуск сервера

Вы можете управлять сервером через графический интерфейс десктопного или мобильного приложения, а также запускать его в безграфических окружениях (headless) через CLI.

### Быстрый запуск (готовый релиз)
```bash
chmod +x ./server/run-server.sh
./server/run-server.sh --pin 1234 --path ~/Documents
```

### Ручной запуск (из исходного кода)
```bash
./gradlew :server:run --args="--pin 1234 --path /vash/put"
```

### Интерактивные команды CLI
После запуска сервер предоставляет консоль управления для ввода команд:

*   `status` — текущее состояние, рабочий порт и список общих папок.
*   `clients` — список подключенных клиентов и статистика передачи данных.
*   `kick <id>` — принудительное завершение сессии клиента по ID.
*   `ip` — локальные IP-адреса сервера и URL-адреса для стриминга.
*   `unban <ip>` — сброс блокировки безопасности (разбан) для указанного IP.
*   `paths` — подробный список расшаренных путей и их состояние.
*   `qr` — вывод параметров подключения в формате JSON.
*   `pin <4-цифры>` — смена PIN-кода доступа на лету.
*   `port <порт>` — изменение рабочего порта сервера.
*   `add <путь>` / `remove <путь>` — управление списком разрешенных директорий.
*   `start` / `stop` — запуск и остановка веб-сервера Ktor.
*   `exit` / `quit` — безопасная остановка и завершение работы приложения.

> *Примечание: Запуск сервера требует обязательной установки 4-значного PIN-кода для обеспечения базовой защиты данных.*

---

## 📥 Загрузка

Актуальные сборки доступны в разделе **[Releases](https://github.com/nim0y/coon-lan-explorer-public/releases)**.

*   **Linux/Unix (CLI-версия):** Скачайте архив `.zip` со страницы релизов.
*   **Windows:** Скачайте установщик `.msi`.
*   **Android:** Доступно в каталоге **[RuStore](https://www.rustore.ru/catalog/app/com.coonstudio.coonlanexplorer)** или в виде `.apk` файлов в релизах GitHub.

---

## 💬 Обратная связь и поддержка

Если вы обнаружили ошибку или хотите предложить функциональное улучшение:
1. Перейдите во вкладку **[Issues](https://github.com/nim0y/coon-lan-explorer-public/issues)**.
2. Убедитесь, что аналогичный запрос отсутствует в списке открытых задач.
3. Создайте новую тему, детально описав сценарий воспроизведения проблемы или концепцию улучшения.

---

*Developed by nim0y with ❤️*
