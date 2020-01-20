# RCT (Right Click Tools) for Updates + Software Update Extension

## English help

## How it looks

- Updates required for members:

![Updates required for members](screenshots/rct-01.png?raw=true "Updates required for the computer")

![Updates required for device](screenshots/SuExt+rct-01.png?raw=true "Updates required for the device")

![Updates required for device collection](screenshots/SuExt+rct-02.png?raw=true "Updates required for the device collection")

- Update compliance status:

![Update compliance status](screenshots/rct-03.png?raw=true "Update compliance status")

![Update compliance status: Required](screenshots/SuExt+rct-03.png?raw=true "Update compliance status")

![Update compliance status: Required](screenshots/SuExt+rct-04.png?raw=true "Update compliance status")

- Create SUG for Collection:

![Create SUG for Collection](screenshots/rct-04.png?raw=true "Create SUG for Collection")

... and more samples from ScreenShots folder

## How to install

- Do backup Console folder "C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole"

- Download ZIP-file, press "Clone or Download" button / "Download ZIP". Unblock file from Properties / Unblock

- Extract All

- For the RCT tool, right-click on "install.bat" and select "Run as Administrator". The bat file will copy RCT *.ps1 and *.xml files.

- For the Console extension, right-click on "install-SuExtension.bat" and select "Run as Administrator". The bat file will copy Software Update Console extension xml-files and ps1 for RCT. Only if your Console supported ("Xml-SuExtension" - the subfolder with Supported version. Now is 1906/1910 )

- Restart the CM-Console

Happy updates!

## Russian

# RCT (Right Click Tools) для работы с обновлениями

- New-RCTSUGByCollection
- Get-RCTUpdateSystemCompliance
- Remove-RCTUpdateFromSUG
- Get-RCTSUCompliance

## New-RCTSUGByCollection

Создаёт Группу обновлений (SUG), которые требуются на членах коллекции устройств. Выбираем группу, правой кнопкой / "Create SUG for Collection"

В группу не входят обновления из категории "Upgrades"

Формат имени для SUG можно задать параметром "-SUGNameTemplate [String]". Вместо {0},{1}…{5} подставляется, соответственно — Год / Месяц / Число / час / минута / секунда.

## Get-RCTUpdateSystemCompliance

Показывает состояние "Required" / "Installed" для конкретного обновления

Скрипт может выводит статус в результирующей таблице в двух режимах:

- Звёздочкой для каждого из состояний

- Один столбец с текстом Required / Installed.

Для включения второго режима добавьте параметр "-StatusInOneColumn" в вызов скрипта в xml файлах.

## Remove-RCTUpdateFromSUG

Удаляет выбранное обновление из всех SUG (Software Update Group).

При выделении папки (контейнера) с обновлениями, удаляет все обновления находящиеся в папке из всех SUG.

## Get-RCTSUCompliance

Показывает обновления требуемые для членов выбранной коллекции устройств.

В список не входят обновления из категории "Upgrades". По умолчанию исключаются обновления с Custom Severity ([-ExcludeCustomSeverity])

## Как установить

Скачиваем ZIP-файл. Разблокируем файл архива – Свойства / Разблокировать.

Распаковываем архив. Запускаем "install.bat" с повышением прав ("Запуск от имени администратора"). Батник скопирует файлы в папку с консолью и покажет результат.

Для установки расширения консоли запускаем "install-SuExtension.bat" с повышением прав ("Запуск от имени администратора"). Батник скопирует файлы в папку с консолью и покажет результат.

Перезапускаем консоль — пользуемся.

Happy updates!
