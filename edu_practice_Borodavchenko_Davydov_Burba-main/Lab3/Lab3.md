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

<img width="993" height="56" alt="image" src="https://github.com/user-attachments/assets/f78a3baf-822a-438e-a6b8-483c0eeb549c" />

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

<img width="1043" height="57" alt="image" src="https://github.com/user-attachments/assets/54762a82-8fbd-41b3-b941-9585913a8bd5" />

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

<img width="973" height="58" alt="image" src="https://github.com/user-attachments/assets/12cceda6-97c1-4d59-84ce-74abadf0c27b" />

*Рис.3 Бурба*

# 2. start.sh

```
#!/bin/bash

echo "Привет, $1!"

```

<img width="426" height="55" alt="image" src="https://github.com/user-attachments/assets/d0480a8f-e79f-4535-8f61-9ff697f6be4c" />

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

<img width="443" height="54" alt="image" src="https://github.com/user-attachments/assets/1250c086-5e66-4278-b7a2-d62e2f02cae6" />

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

<img width="334" height="95" alt="image" src="https://github.com/user-attachments/assets/eab51380-1df0-4143-8c91-8e8d30dcbe95" />

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

<img width="305" height="74" alt="image" src="https://github.com/user-attachments/assets/6e7e3aff-d16a-40f1-8a69-7ef56b7818a1" />

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

<img width="310" height="94" alt="image" src="https://github.com/user-attachments/assets/ff0c98a8-c1a3-4325-80f3-05e1b04fc56c" />

*Рис.8 Запуск скрипта на создание и проверку директории*

# 7 user_light.sh

```
#!/bin/bash

my_user=$(whoami)
if grep -q "^$my_user:" /etc/passwd; then
    echo "Поздравляю! Пользователь '$my_user' найден в системе."
fi
```

<img width="452" height="58" alt="image" src="https://github.com/user-attachments/assets/b1f8485f-106d-4278-8e36-97ae0622c204" />

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

<img width="316" height="95" alt="image" src="https://github.com/user-attachments/assets/397dc13a-c10d-4d24-a901-7d08a2b56086" />

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

<img width="529" height="77" alt="image" src="https://github.com/user-attachments/assets/72c8a56e-4ae9-4219-8751-1a262dffdc24" />

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

<img width="409" height="132" alt="image" src="https://github.com/user-attachments/assets/4331d9fc-8989-40fe-a473-688f0dcb6035" />

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

<img width="284" height="95" alt="image" src="https://github.com/user-attachments/assets/27f91e8a-f5f0-45b7-9aba-b76c528c9da7" />

*Рис.13 Вывод результата math.sh*

# 12 sort.sh

```
#!/bin/bash

for arg in "$@"; do
    echo "$arg"
done
```

<img width="355" height="114" alt="image" src="https://github.com/user-attachments/assets/1a6bba72-be6d-408d-a571-abf6cd01a538" />

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

<img width="314" height="172" alt="image" src="https://github.com/user-attachments/assets/5b461269-0de0-4120-86de-4e5e62d5fe2f" />

*Рис.15 Прием аргументов*

# 14 user_use.sh

```
#!/bin/bash

du -sk /home/* 2>/dev/null | sort -nr | while read size dir; do
    user=$(basename "$dir")
    echo "$user — $size КБ"
done
```

<img width="329" height="54" alt="image" src="https://github.com/user-attachments/assets/87cc24db-0293-45ce-8dcd-f22431354795" />

*Рис.16 Вывод пользователя по занятому месту*

# 15 sort_du.sh

```
#!/bin/bash

dir="${1:-.}"
find "$dir" -type f -printf '%T@ %p\n' 2>/dev/null | sort -n | head -3 | while read timestamp path; do
    date=$(date -d "@$timestamp" "+%Y-%m-%d %H:%M:%S")
    echo "$path — $date"
done
```

<img width="335" height="93" alt="image" src="https://github.com/user-attachments/assets/977fe526-4942-48a4-8bb7-ee5f1d7161d3" />

*Рис.17 Вывод 3 самый последних файлов*

# 16 dir_info.sh

```
#!/bin/bash

dir="${1:-.}"
size=$(du -sk "$dir" | awk '{print $1}')
echo "Общий размер: $size КВ"
```

<img width="658" height="129" alt="image" src="https://github.com/user-attachments/assets/3366a473-8187-4691-a8fa-b3ef24a14eb8" />

*Рис.18 Вывод общего размера в кб*

# 17 bash_history.sh

```
#!/bin/bash

hist_file="$HOME/.bash_history"
if [ -f "$hist_file" ]; then
    awk '{print $1}' "$hist_file" | sort | uniq -c | sort -nr | head -5
else
    echo "Файл .bash_history не найден."
fi
```

<img width="361" height="132" alt="image" src="https://github.com/user-attachments/assets/947d69ce-99f3-4bf9-a21c-0d58380a1674" />

*Рис.19 Вывод 5 самых используемых команд*



