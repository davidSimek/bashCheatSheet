# Bash bashcheat-sheet

## Variables
```bash
name="John"                         # Assign a value to a variable
echo "Hello, $name!"                # Print a personalized greeting
```

## Command Execution
```bash
output=$(ls)                        # Execute 'ls' command and capture its output
echo "$output"                      # Print the captured output

```
## Conditional Statements
```bash
if [[ $name == "John" ]]; then
    echo "Name is John"              # Code executed if the condition is true
else
    echo "Name is not John"          # Code executed if the condition is false
fi

```
## Looping
```bash
for i in {1..5}; do
    echo "Iteration $i"              # Code executed for each iteration of the loop
done

```
## String Operations
```bash
sentence="Hello, World!"
echo "${#sentence}"                  # Print the length of the string
echo "${sentence:7:5}"               # Print a substring ("World")
echo "${sentence//o/O}"              # Replace all occurrences of "o" with "O"

```
## File Operations
```bash
cat myfile.txt                       # Display the contents of a file
echo "New text" > myfile.txt         # Write text to a file (overwriting existing contents)
echo "Additional text" >> myfile.txt # Append text to a file
cp source.txt destination.txt        # Copy a file
mv oldname.txt newname.txt           # Rename a file
rm unwanted.txt                      # Remove a file

```
## Directory Operations
```bash
ls                                   # List files and directories in the current directory
pwd                                  # Print the current working directory
cd mydir                             # Change to a different directory
mkdir newdir                         # Create a new directory
rmdir emptydir                       # Remove an empty directory
cp -r sourcedir destinationdir       # Copy a directory and its contents recursively
mv olddir newdir                     # Rename a directory
rm -r unwanteddir                    # Remove a directory and its contents recursively

```
## Permissions
```bash
chmod u+u+xx myfile.txt                 # Change permissions of a file

```
## Input/Output
```bash
read input_variable                  # Read user input and assign it to a variable
echo "You entered: $input_variable"  # Print the user input

```
## Exit Status
```bash
ls                                   # Execute a command
echo "Exit status: $?"               # Print the exit status of the previous command

```
## While Loop
```bash
counter=0
while [[ $counter -lt 5 ]]; do
    echo "Iteration: $counter"
    counter=$((counter + 1))
done

```
## Arithmetic Operations
```bash
result=$((2 + 3))
echo "Result: $result"

```
## Arrays
```bash
fruits=("apple" "banana" "orange")
echo "First fruit: ${fruits[0]}"
echo "All fruits: ${fruits[@]}"

```
## Command-Line Arguments
```bash
echo "Script Name: $0"
echo "First Argument: $1"
echo "Number of Arguments: $#"
echo "All Arguments: $@"

```
## Conditionals: Case Statement
```bash
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

```
## Command Substitution
```bash
files_count=$(ls | wc -l)
echo "Number of files: $files_count"

```
## Conditional Expressions
```bash
if [[ $name == "John" ]]; then
    echo "Name is John"
else
    echo "Name is not John"
fi

```
## Iterating Through a Directory
```bash
for file in /path/to/directory/*; do
    echo "File: $file"
done

```
## Regular Expressions
```bash
if [[ $name =~ ^J.*n$ ]]; then
    echo "Name starts with 'J' and ends with 'n'"
else
    echo "Name does not match the pattern"
fi
```
