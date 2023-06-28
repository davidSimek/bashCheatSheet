# Bash cheat-sheet

```
#!/bin/bash

# Comments start with a '#' symbol

# Variables
name="John"                         # Assign a value to a variable
echo "Hello, $name!"                # Print a personalized greeting

# Command Execution
output=$(ls)                        # Execute 'ls' command and capture its output
echo "$output"                      # Print the captured output

# Conditional Statements
if [[ $name == "John" ]]; then
    echo "Name is John"              # Code executed if the condition is true
else
    echo "Name is not John"          # Code executed if the condition is false
fi

# Looping
for i in {1..5}; do
    echo "Iteration $i"              # Code executed for each iteration of the loop
done

# String Operations
sentence="Hello, World!"
echo "${#sentence}"                  # Print the length of the string
echo "${sentence:7:5}"               # Print a substring ("World")
echo "${sentence//o/O}"              # Replace all occurrences of "o" with "O"

# File Operations
cat myfile.txt                       # Display the contents of a file
echo "New text" > myfile.txt         # Write text to a file (overwriting existing contents)
echo "Additional text" >> myfile.txt # Append text to a file
cp source.txt destination.txt        # Copy a file
mv oldname.txt newname.txt           # Rename a file
rm unwanted.txt                      # Remove a file

# Directory Operations
ls                                   # List files and directories in the current directory
pwd                                  # Print the current working directory
cd mydir                             # Change to a different directory
mkdir newdir                         # Create a new directory
rmdir emptydir                       # Remove an empty directory
cp -r sourcedir destinationdir       # Copy a directory and its contents recursively
mv olddir newdir                     # Rename a directory
rm -r unwanteddir                    # Remove a directory and its contents recursively

# Permissions
chmod 755 myfile.txt                 # Change permissions of a file

# Input/Output
read input_variable                  # Read user input and assign it to a variable
echo "You entered: $input_variable"  # Print the user input

# Exit Status
ls                                   # Execute a command
echo "Exit status: $?"               # Print the exit status of the previous command

# Examples
echo "Hello, World!"                 # Print "Hello, World!"
ls                                  # List files and directories in the current directory
mkdir new_directory                 # Create a new directory

# Algorithmic Parts
# While Loop
counter=0
while [[ $counter -lt 5 ]]; do
    echo "Iteration: $counter"
    counter=$((counter + 1))
done

# Arithmetic Operations
result=$((2 + 3))
echo "Result: $result"

# Arrays
fruits=("apple" "banana" "orange")
echo "First fruit: ${fruits[0]}"
echo "All fruits: ${fruits[@]}"

# Command-Line Arguments
echo "Script Name: $0"
echo "First Argument: $1"
echo "Number of Arguments: $#"
echo "All Arguments: $@"

# Conditionals: Case Statement
option="start"
case $option in
    "start")
        echo "Starting the application..."
        ;;
    "stop")
        echo "Stopping the application..."
        ;;
    *)
        echo "Unknown option"
        ;;
esac

# Command Substitution
files_count=$(ls | wc -l)
echo "Number of files: $files_count"

# Conditional Expressions
if [[ $name == "John" ]]; then
    echo "Name is John"
else
    echo "Name is not John"
fi

# Iterating Through a Directory
for file in /path/to/directory/*; do
    echo "File: $file"
done

# Regular Expressions
if [[ $name =~ ^J.*n$ ]]; then
    echo "Name starts with 'J' and ends with 'n'"
else
    echo "Name does not match the pattern"
fi
```
