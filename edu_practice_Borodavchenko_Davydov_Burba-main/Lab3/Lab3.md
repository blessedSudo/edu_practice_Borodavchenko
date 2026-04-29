# 1. zero.sh

Давыдов :

```
#!/bin/bash

group="321"
name="Матвей"
surname="Давыдов"
stipendia=778
usd_rate=75
usd_sum=$((stipendia / usd_rate))

echo "Я учусь в $group, зовут меня $name $surname. В этом месяце мне пришла стипендия размером в $stipendia рублей, это $usd_sum $."

```

<img width="885" height="49" alt="изображение" src="https://github.com/user-attachments/assets/c672b618-2efb-417d-a64e-5d9f4b868f90" />

*Рис.1 Давыдов*

Бородоваченко :

```
#!/bin/bash

group="321"
name="Даниил"
surname="Бородавченко"
stipendia=778
usd_rate=75
usd_sum=$((stipendia / usd_rate))

echo "Я учусь в $group, зовут меня $name $surname. В этом месяце мне пришла стипендия размером в $stipendia рублей, это $usd_sum $."

```

<img width="934" height="37" alt="изображение" src="https://github.com/user-attachments/assets/3a9397ae-9ca6-47a0-a5cd-71e803d780cb" />

*Рис.2 Бородавченко*

Бурба :

```
#!/bin/bash

group="321"
name="Ульяна"
surname="Бурба"
stipendia=778
usd_rate=75
usd_sum=$((stipendia / usd_rate))

echo "Я учусь в $group, зовут меня $name $surname. В этом месяце мне пришла стипендия размером в $stipendia рублей, это $usd_sum $."

```

<img width="871" height="44" alt="изображение" src="https://github.com/user-attachments/assets/97aa4f47-f325-465f-b492-180a624a51f3" />

*Рис.3 Бурба*

# 2. start.sh

```
#!/bin/bash

echo "Привет, $1!"

```

<img width="250" height="19" alt="изображение" src="https://github.com/user-attachments/assets/538a4ad4-8af7-4ae1-9406-14815f18c852" />

*Рис.4 Запуск файла start.sh*

# 3. start_2.sh

```
#!/bin/bash

if [ -n "$1" ]; then
    echo "Привет, $1!"
else
    echo "Имя не передано."
fi
```

<img width="405" height="33" alt="изображение" src="https://github.com/user-attachments/assets/d13a415e-2e94-4525-8f1e-43d41d2e5ad9" />

*Рис.5 Запуск start_2.sh*

# 4 file.sh

```
#!/bin/bash

if [ -e "$1" ]; then
    echo "Файл '$1' существует."
else
    echo "Файл '$1' не найден."
fi
```

<img width="295" height="68" alt="изображение" src="https://github.com/user-attachments/assets/116c6afa-c85e-4a1c-942f-9d975d93d62f" />

*Рис.6 Запуск file.sh*

# 5 my_dir.sh

```
#!/bin/bash

if [ -d "$1" ]; then
    ls "$1"
else
    echo "Директория '$1' не найдена."
fi

```

<img width="281" height="86" alt="изображение" src="https://github.com/user-attachments/assets/e7f16f3a-e561-459a-81b0-5832bbea1061" />

*Рис.7 Запуск my_dir.sh /home*

# 6 dir_m.sh

```
#!/bin/bash

if [ -d "$1" ]; then
    echo "Директория '$1' уже существует."
else
    mkdir "$1"
    echo "Директория '$1' создана."
fi

```

<img width="291" height="103" alt="изображение" src="https://github.com/user-attachments/assets/585831c4-553e-416f-b88d-87ea8266a7ff" />

*Рис.8 Запуск скрипта на создание и проверку директории*

# 7 user_light.sh

```
#!/bin/bash

my_user=$(whoami)
if grep -q "^$my_user:" /etc/passwd; then
    echo "Поздравляю! Пользователь '$my_user' найден в системе."
fi
```

<img width="400" height="41" alt="изображение" src="https://github.com/user-attachments/assets/d6225c1f-f7d1-4791-a5cc-d2d5c7e633a2" />

*Рис.9 Проверям пользователя*

# 8 user_f.sh

```
#!/bin/bash

if grep -q "^$1:" /etc/passwd; then
    echo "Пользователь '$1' найден."
else
    echo "Пользователь '$1' не найден."
fi
```

<img width="267" height="87" alt="изображение" src="https://github.com/user-attachments/assets/d1cfc5f1-4b33-4791-b796-a92bb22bb1cd" />

*Рис.10 Проверяем пользователя*

# 9 user_f2.sh

```
#!/bin/bash

if [ -z "$1" ]; then
    echo "Укажите имя пользователя!"
    exit 1
fi

if grep -q "^$1:" /etc/passwd; then
    echo "Пользователь '$1' найден в системе!"
else
    echo "Пользователь '$1' не найден!"
    filename="don't_be_sad_user_${1}_will_be_there_soon.txt"
    touch "$filename"
    echo "Создан файл: $filename"
fi
```

<img width="478" height="70" alt="изображение" src="https://github.com/user-attachments/assets/64218998-6a7c-480b-8dd8-fba813467747" />

*Рис.11 Усовершенствованный код*

# 10 finder_light.sh

```
#!/bin/bash

if [ -f "$1" ]; then
    echo "'$1' — обычный файл."
elif [ -d "$1" ]; then
    echo "'$1' — директория."
elif [ -L "$1" ]; then
    echo "'$1' — символическая ссылка."
else
    echo "'$1' — не существует или другой тип."
fi
```

<img width="343" height="101" alt="изображение" src="https://github.com/user-attachments/assets/9e086a93-8048-42f8-a68c-15a9a85f62a6" />

*Рис.12 Определение файла*

# 11 math.sh

```
#!/bin/bash

a=$1
b=$2

echo "Сумма: $((a + b))"
echo "Разность: $((a - b))"
echo "Произведение: $((a * b))"
```

<img width="273" height="97" alt="изображение" src="https://github.com/user-attachments/assets/c992c0f9-d535-4649-8af6-32b718736c2c" />

*Рис.13 Вывод результата math.sh*

# 12 sort.sh

```
#!/bin/bash

for arg in "$@"; do
    echo "$arg"
done
```

<img width="298" height="63" alt="изображение" src="https://github.com/user-attachments/assets/6759b123-3dd8-49b7-984a-24d9afba231f" />

*Рис.14 Вывод аргументов*

# 13 io.sh

```
#!/bin/bash

case "$1" in
    start) echo "Starting..." ;;
    stop)  echo "Stopping..." ;;
    *)     echo "Используй: $0 {start|stop}" ;;
esac
```

<img width="242" height="86" alt="изображение" src="https://github.com/user-attachments/assets/4b57897f-6122-49d0-a3b5-ac992d3265c7" />

*Рис.15 Прием аргументов*

# 14 user_use.sh

```
#!/bin/bash

du -sk /home/* 2>/dev/null | sort -nr | while read size dir; do
    user=$(basename "$dir")
    echo "$user — $size КБ"
done
```

<img width="302" height="56" alt="изображение" src="https://github.com/user-attachments/assets/aba09ae7-cfa8-4eff-8681-430c65d4231d" />

*Рис.16 Вывод пользователя по занятому месту*

# 15 sort_du.sh

```
#!/bin/bash

dir=${1:-.}
find "$dir" -maxdepth 1 -type f -exec stat -c "%x %n" {} + | sort | head -n 3
```

<img width="465" height="77" alt="изображение" src="https://github.com/user-attachments/assets/a0473ae3-796f-46c4-86a8-f68d1a8a1d6f" />

*Рис.17 Вывод 3 самый последних файлов*

# 16 dir_info.sh

```
#!/bin/bash

dir="${1:-.}"
size=$(du -sk "$dir" | awk '{print $1}')
echo "Общий размер: $size КВ"
```

<img width="288" height="52" alt="изображение" src="https://github.com/user-attachments/assets/7d28dfd9-a269-4674-9ea5-3d5dca943040" />

*Рис.18 Вывод общего размера в кб*

# 17 bash_history.sh

```
#!/bin/bash
history -a
cat ~/.bash_history | awk "{print \$1" | sort | uniq -c | sort -nr | head -n 5 > bash_history.sh
```

<img width="204" height="110" alt="изображение" src="https://github.com/user-attachments/assets/95b0c639-27a1-44f1-be36-4aaf46674c1a" />

*Рис.19 Вывод 5 самых используемых команд*



