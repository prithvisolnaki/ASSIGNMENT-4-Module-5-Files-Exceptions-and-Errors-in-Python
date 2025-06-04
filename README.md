# ASSIGNMENT-4-Module-5-Files-Exceptions-and-Errors-in-Python

This assignment includes two tasks that demonstrate basic file handling operations and exception handling using Python.

---

## ✅ Task 1: Read a File and Handle Errors

### 📝 Problem Statement:
Write a Python program that:
1. Opens and reads a text file named `sample.txt`.
2. Prints its content line by line.
3. Handles errors gracefully if the file does not exist.

### 💻 Code:


# Create sample.txt 
file = open("sample.txt", "w")
file.write("Line 1: This is a sample text file\n")
file.write("Line 2: It contains multiple lines\n")
file.close()

# Try to read the file with error handling
try:
    file = open("sample.txt", "r")
    for line in file:
        print(line.strip())
    file.close()
except FileNotFoundError:
    print("The file 'sample.txt' was not found.")

****Output:

Line 1: This is a sample text file
Line 2: It contains multiple lines

If File is Missing (e.g., sample1.txt):
**CODE: **
try:
    file = open("sample1.txt", "r")
    for line in file:
        print(line.strip())
    file.close()
except FileNotFoundError:
    print("The file 'sample1.txt' was not found.")

**✅ Task 2: Write and Append Data to a File**
📝 Problem Statement:
Write a Python program that:
Takes user input and writes it to a file named output.txt.
Appends additional data to the same file.
Reads and displays the final content of the file.
**Code:**
# Take user input and write to the file
text1 = input("Enter text to write to the file: ")
with open("output.txt", "w") as file:
    file.write(text1 + "\n")
print("Data Successfully written to output.txt.")

# Append more text to the same file
text2 = input("Enter additional text to append to the file: ")
with open("output.txt", "a") as file:
    file.write(text2 + "\n")
print("Data Successfully appended.")

# Read and display the final content of the file
print("\nFinal content of output.txt:")
with open("output.txt", "r") as file:
    for line in file:
        print(line.strip())

**Output   **     
Enter text to write to the file: Hello, Python
Data Successfully written to output.txt.
Enter additional text to append to the file: Learning file handling in Python
Data Successfully appended.

Final content of output.txt:
Hello, Python
Learning file handling in Python
