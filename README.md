# 🦝 CoonLanExplorer
**Ваш личный мост между устройствами в локальной сети.**

CoonLanExplorer — это кроссплатформенный файловый менеджер и инструмент для обмена данными, позволяющий управлять файлами на компьютере напрямую с мобильного устройства или другого ПК в пределах одной локальной сети. Данные передаются напрямую между устройствами без использования внешних серверов или облачных хранилищ.

*Этот репозиторий является публичной точкой доступа к проекту: здесь публикуются официальные релизы, ведется документация и принимаются сообщения об ошибках (Issues).*

[English](#features-en) | [Русский](#возможности-ru)

---

## 📸 Скриншоты (Screenshots)

<p align="center">
  <img src="screenshots/Screenshot 2026-06-02 222705.png" width="600" alt="Desktop Interface">
  <img src="screenshots/Screenshot 2026-06-02 222724.png" width="600" alt="Desktop Interface">
  <img src="screenshots/Screenshot 2026-06-02 222811.png" width="600" alt="Desktop Interface">
  <img src="screenshots/Screenshot 2026-06-02 222822.png" width="600" alt="Desktop Interface">
</p>
  
  ---
  
## 📸 Скриншоты мобильная версия (Screenshots)

<p align="center">
  <img src="screenshots/Screenshot 2026-06-02 222848.png" width="300" alt="Mobile Explorer">
  <img src="screenshots/Screenshot 2026-06-02 222900.png" width="300" alt="Mobile Explorer">
  <img src="screenshots/Screenshot 2026-06-02 222911.png" width="300" alt="Mobile Explorer">
  <img src="screenshots/Screenshot 2026-06-02 222921.png" width="300" alt="Mobile Explorer">
  <img src="screenshots/Screenshot 2026-06-02 222931.png" width="300" alt="Mobile Explorer">
  <img src="screenshots/Screenshot 2026-06-02 222939.png" width="300" alt="Mobile Explorer">
</p>
<p align="center">
  <i>Интерфейс приложения на Desktop и Android</i>
</p>

---

<a name="возможности-ru"></a>
## ✨ Основные возможности

*   **⚡ Мгновенное подключение:** Просто отсканируйте QR-код на экране монитора своим смартфоном — и вы уже внутри файловой системы.
*   **🛡 Безопасность военного уровня:** Все данные шифруются (AES-256-GCM + ECDH). Доступ защищен обязательным PIN-кодом, который вы задаете сами.
*   **🔍 Автопоиск в сети:** Приложение само найдет запущенный сервер в вашей Wi-Fi сети.
*   **📦 Умная загрузка:** Скачивайте файлы по одному или целыми папками (автоматически упаковываются в ZIP).
*   **🖥 Удаленное управление:** Открывайте документы или запускайте видео на компьютере прямо с телефона.
*   **🚀 Полный контроль:** Управляйте сервером, смотрите список подключенных клиентов и настраивайте права доступа в пару кликов.

---

## 📥 Загрузка (Download)

Вы можете скачать актуальную версию для вашей платформы в разделе **[Releases](https://github.com/nim0y/coon-lan-explorer-public/releases)**.

*   **Windows:** Скачайте `.msi` установщик.
*   **Android:** Скоро в RuStore / Скачайте `.apk` из релизов.

---

## 🛠 Технологии (Tech Stack)

Приложение разработано с использованием следующих технологий:
*   **Kotlin Multiplatform (KMP)** — общая бизнес-логика и сетевое взаимодействие для всех платформ.
*   **Compose Multiplatform** — декларативный пользовательский интерфейс для Android и Desktop.
*   **Ktor (Client & Server)** — встроенный легковесный веб-сервер и сетевой клиент.
*   **Coroutines & Flow** — асинхронное выполнение операций ввода-вывода.

---

## 💬 Обратная связь и поддержка

Если вы столкнулись с ошибкой или хотите предложить новую функцию:
1. Перейдите во вкладку **[Issues](https://github.com/nim0y/coon-lan-explorer-public/issues)**.
2. Проверьте, нет ли схожей проблемы в списке открытых.
3. Если проблема не найдена, создайте новое обращение, подробно описав шаги для воспроизведения бага или суть вашего предложения.

---

*Developed by nim0y with ❤️*

---

<a name="features-en"></a>
# 🦝 CoonLanExplorer

**Your personal bridge between devices on the local network.**

CoonLanExplorer is a cross-platform file manager and file-sharing solution that allows you to access and manage files on your computer directly from a smartphone or another PC within the same local network.

All communication happens directly between your devices without relying on cloud storage or third-party servers.

> This repository serves as the public hub for the project, where official releases, documentation, and issue tracking are maintained.

---

## ✨ Features

* **⚡ Instant Connection**
  Scan a QR code displayed on your desktop and connect to your file system in seconds.

* **🛡 Secure Communication**
  Data is protected using modern encryption (AES-256-GCM + ECDH) and secured with a user-defined PIN code.

* **🔍 Automatic Network Discovery**
  Automatically detect available servers within your local Wi-Fi or LAN.

* **📦 Smart Downloads**
  Download individual files or entire directories. Folders are automatically packaged as ZIP archives.

* **🖥 Remote Actions**
  Open documents, launch applications, or play media on your desktop directly from your mobile device.

* **🚀 Full Control**
  Monitor connected clients, manage access permissions, and configure server settings with ease.

---

## 🔒 Security

Security is a core part of the project architecture.

* Each connection establishes a unique encrypted session.
* A user-defined PIN participates in key generation and access protection.
* Session tokens are temporary and automatically expire.
* File access is restricted to explicitly allowed directories.
* Data remains inside your local network and is never routed through external cloud services.

---

## 📥 Download

The latest releases are available in the Releases section.

* **Windows:** MSI installer
* **Android:** APK package (RuStore release available)

---

## 🛠 Tech Stack

Built with:

* **Kotlin Multiplatform (KMP)** — shared business logic and networking
* **Compose Multiplatform** — modern UI for Android and Desktop
* **Ktor Client & Server** — embedded networking stack
* **Coroutines & Flow** — asynchronous and reactive programming

---

## 💬 Feedback & Support

Found a bug or have an idea for improvement?

1. Open the **Issues** tab.
2. Check whether a similar issue already exists.
3. Create a new issue with detailed reproduction steps or a feature request.

Feedback and contributions to the project roadmap are always welcome.

---

*Developed by nim0y with ❤️*

---
