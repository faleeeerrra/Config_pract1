# Task1
```
grep ':' /etc/passwd | cut -d':' -f1 | sort
```
![image](https://github.com/user-attachments/assets/77f2276a-e122-4db4-8f6e-41ad8e1da139)
***

# Task2
```
cat /etc/protocols | awk '{print $2, $1}' | sort -nr | head -5
```
![image](https://github.com/user-attachments/assets/2a97764c-2e40-4820-bd2a-a87e6fb6a3d4)
***

# Task 3
```
#!/bin/bash
text=$1
size=${#text}
echo -n "+"
for ((i = -2; i < size; i++))
do
echo -n "-"
done
echo "+"
echo "| $text |"
echo -n "+"
for ((i = -2; i < size; i++))
do
echo -n "-"
done
echo "+"
```
![image](https://github.com/faleeeerrra/Config_pract1/blob/main/image.png)
***

# Task4
```
grep -o '\b[a-zA-Z_][a-zA-Z0-9_]*\b' hello.py | sort | uniq
```
![image](https://github.com/user-attachments/assets/8ec2d314-deba-4f0f-9e51-b3762efe5b7b)
***

# Task 5
Написать программу для регистрации пользовательской команды (правильные права доступа и копирование в /usr/local/bin).

Например, пусть программа называется reg:
```
./reg banner
```
В результате для banner задаются правильные права доступа и сам banner копируется в /usr/local/bin.
```
#!/bin/bash
 
if [ "$#" -ne 1 ]; then
        echo "Использование: $0 <имя_файла>"
        exit 1
fi
 
COMMAND=$1
 
 
if [ ! -f "$COMMAND" ]; then
        echo "Ошибка: файл $COMMAND не существует."
        exit 1
fi
 
sudo cp "$COMMAND" /usr/local/bin/
 
if [ $? -ne 0 ]; then
        echo "Ошибка: не удалось скопировать файл в /usr/local/bin."
        exit 1
fi
 
sudo chmod 755 /usr/local/bin/"$COMMAND"
 
if [ $? -ne 0 ]; then
        echo "Ошибка: не удалось установить права доступа."
        exit 1
fi
 
echo "Команда $COMMAND успешно зарегистрирована в /usr/local/bin."
```
![image](https://github.com/user-attachments/assets/df90b789-6011-467e-b566-6560b36ef5dd)
***


