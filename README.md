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

<a name="features-en"></a>
## ✨ Key Features

*   **Fast Connection:** Scan a QR code to link your devices without entering IP addresses manually.
*   **Encrypted Channel:** Data protection using AES-256-GCM encryption with ECDH key exchange.
*   **Network Discovery:** Automatic discovery of active servers in the local Wi-Fi/LAN network.
*   **Batch Operations:** Transfer folders as zip-archives generated on-the-fly.
*   **Remote Actions:** Open documents or play media on your desktop machine directly from your phone.
*   **Access Control:** Configure read-only modes and restrict access to specific directories.

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
