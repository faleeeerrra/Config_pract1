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
