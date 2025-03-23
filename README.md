# XBC1 и ARD/ARH Архиватор

Tool this https://github.com/Nenkai/XbxDeTool

Инструмент для работы с форматами файлов Xenoblade Chronicles: XBC1, ARD и ARH.

## Возможности

- Распаковка XBC1 файлов
- Упаковка файлов в формат XBC1
- Распаковка ARD архивов с использованием ARH файлов
- Создание новых ARD/ARH архивов
- Фильтрация файлов по типу (например, только BDAT)
- Многопоточная обработка для высокой производительности

## Установка

```bash
# Установка зависимостей
pip install zstandard tqdm
```

## Использование

### Распаковка XBC1 файла

```bash
python xbc1_tool.py input.xbc1 [output_file]
```

### Упаковка файла в XBC1

```bash
python xbc1_tool.py input.bin -c [output_file]
```

### Распаковка ARD архива

```bash
# Распаковка всех файлов
python xbc1_tool.py --ard game.ard game.arh [output_directory]

# Распаковка только BDAT файлов
python xbc1_tool.py --ard game.ard game.arh [output_directory] --only-bdat
```

### Создание ARD архива

```bash
# Создание архива без сжатия файлов
python xbc1_tool.py --create-ard input_directory output.ard output.arh

# Создание архива со сжатием файлов
python xbc1_tool.py --create-ard input_directory output.ard output.arh --compress-files
```
