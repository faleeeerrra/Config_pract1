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


