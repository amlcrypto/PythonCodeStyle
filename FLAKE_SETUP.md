## Настройка линтера
Поскольку мы приняли коллективное решение не усложнять себе жизнь, линтер будет жить в IDE разработчиков без особенных настроек.

Т.к. большинство разработчиков пользуется VSCode, линтер настраивается следующим образом:
1. Необходимо установить расширение flake8 через встроенный магазин расширений. 
    - Вариант А: Панель слева -> ввести flake8 в поиске -> Прожать "установить"
    - Вариант В: Открыть командную панель (Ctrl+Shift+P) -> Вставить команду ext install ms-python.flake8
2. По умолчанию линтер подхватит .flake8 файл в репозитории.
3. При создании нового репозитория необходимо скопировать .flake8 файл из данного репозитория.

## Продвинутая настройка линтера
Когда мы решим, что базового линтинга недостаточно, необходимо будет добавить плагины флейка. На данный момент в конфигурации использованы `flake8 flake8-docstrings flake8-import-order` (опции неустановленных плагинов игнорируются). Их необходимо будет добавить в виртуальное окружение через `pip install flake8 flake8-docstrings flake8-import-order`, возможно, необходимо будет создать requirements.dev.txt и добавить зависимости туда.
