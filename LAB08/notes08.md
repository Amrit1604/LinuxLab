# LAB EXPERIMENT -8

**1.** **System Infomation Script: Write shell scripts to print system information.**

```
#!/bin/bash
lscpu
```
![INFO](https://github.com/user-attachments/assets/55c0bc74-2c96-461c-98ca-e71046b74344)

**2.** **Arithmetic Calculation: Write shell script to perform basic mathematical calculation.**
```
#!/bin/bash

echo "Enter 1st number"
read num1
echo "Enter 2nd number"
read num2
echo "Enter the operator you want to use (+, -, *, /)"
read op

case $op in
+) result=$((num1 + num2))
     echo "Result: $result"
     echo "Result: $result" >> result.txt ;;

  -) result=$((num1 - num2))
     echo "Result: $result"
     echo "Result: $result" >> result.txt ;;

  \*) result=$((num1 * num2))
     echo "Result: $result"
     echo "Result: $result" >> result.txt ;;

  /) if [ "$num2" -ne 0 ]; then
       result=$((num1 / num2))
       echo "Result: $result"
       echo "Result: $result" >> result.txt
     else
       echo "Error: Division by zero is not allowed" >> result.txt
     fi ;;

  *) echo "Invalid operator";;
esac
```

![airthmetic](https://github.com/user-attachments/assets/a23d7a5b-7e5b-4da4-ba8f-b0cfe45db725)

**3.** **Redirect Output: Use redirection operators to store the output of commands.**

```
#!/bin/bash

while true; do
echo "---------------------------"
echo "Please select an option:"
echo "1: Display the current date and time"
echo "2: Show the list of files in the current directory"
echo "3: Display the current working directory"
echo "4: Exit the script"
echo "---------------------------"
read -p "Enter your choice (1-4): " choice
case $choice in
1)
echo "Current date and time: $(date)" >> date.txt
;;
2)
echo "Files in the current directory:" >> file.txt
ls
;;
3)
echo "Current working directory: $(pwd)" >> dir.txt
;;
4)
echo "Exiting the script. Goodbye!"
break
;;
*)
echo "Invalid choice. Please select a valid option (1-4)."
;;
esac
echo ""
done
```
![redirect](https://github.com/user-attachments/assets/5862f629-3710-4375-a981-8565488e71b7)

![all](https://github.com/user-attachments/assets/87b0b30f-2190-4485-a01a-f2ab0364819a)

