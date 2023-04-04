# Lesson 3: Variables and Operators

## Declaring and using variables

Variables in Bash are used to store and manipulate data in scripts. To declare a variable, you can assign a value to it using the `=` operator. For example, to declare a variable named `name` with the value "John", you can type:
```bash
name="John"
```
**Warning**: no spaces between variable name, operator and value.


To access the value of a variable, you can use the `$` symbol followed by the variable name. For example, to print the value of the `name` variable, you can type: 
```bash
echo $name
```
You can also use double quotes to include variables in a string. For example, to print a message that includes the `name` variable, you can type: 
```bash
echo "Hello, $name!"
```
## Basic variable types

Bash supports several basic variable types, including strings, integers, and arrays. When declaring a variable, you do not need to specify the data type explicitly. Bash will automatically determine the data type based on the value assigned to the variable.

### Strings

String variables are used to store text data. To declare a string variable, you can assign a value enclosed in quotes. For example:

```bash
greeting="Hello, world!"
```
You can concatenate strings in Bash. For example:
```bash
first_name="John"
last_name="Doe"
full_name=$first_name" "$last_name #or "${first_name} ${last_name}"
echo $full_name # will output 'John Doe'
```
### Integers

Integer variables are used to store numeric data. To declare an integer variable, you can assign a value without quotes. For example:
```bash
age=25
```
You can perform arithmetic operations on integer variables using arithmetic operators. For example:
```bash
x=5
y=10
z=$((x + y))
echo $z # output 15
```
**Warning**: In Bash, arithmetic expressions are evaluated using the `$(( ))` syntax. When you use a double pair of parentheses around an arithmetic expression, Bash knows to evaluate the expression and return the result as an integer. The `$(( ))` syntax is used to perform arithmetic operations on variables or constants, and the result of the expression can be assigned to a variable using the standard variable assignment syntax (variable_name=expression). It's important to note that the `$(( ))` syntax is used only for arithmetic expressions, and it does not work with string or boolean expressions. 

### Arrays

Array variables are used to store multiple values. To declare an array variable, you can assign a list of values enclosed in parentheses. For example:

```bash
fruits=("apple" "banana" "orange")
```
You can access the values of an array using the ${} notation followed by the index of the value. For example:
```bash
echo ${fruits[0]} # output "apple"
```

## Using arithmetic and comparison operators

Bash supports several arithmetic and comparison operators that can be used to perform mathematical calculations and compare values. Arithmetic operators include `+` for addition, `-` for subtraction, `*` for multiplication, `/` for division, and `%` for modulus. Comparison operators include `-eq` for equal to, `-ne` for not equal to, `-lt` for less than, `-le` for less than or equal to, `-gt` for greater than, and `-ge` for greater than or equal to.

### Arithmetic operators

You can use arithmetic operators to perform mathematical calculations on integer variables. For example:
```bash
x=5
y=10
z=$((x + y))
echo $z
```
### Comparison operators

You can use comparison operators to compare the values of variables. For example:

```bash
x=5
y=10
if [ $x -lt $y ]
then
    echo "$x is less than $y"
else
    echo "$x is not less than $y"
fi # output "5 is less than 10"
```

## Best practices for naming variables

When naming variables in Bash, it is important to choose names that are descriptive and easy to understand. Variable names should start with a letter and can include letters, numbers, and underscores. It is best to use lowercase letters for variable names, as uppercase letters can cause errors in some cases. Additionally, it is important to avoid using reserved keywords or names that conflict with other variables or functions in the script.

Here are some additional tips for naming variables in Bash:

- Choose names that are descriptive and easy to understand. For example, instead of using x or y as variable names, use more descriptive names like total or count.

- Use underscores to separate words in variable names. For example, use first_name instead of firstname.

- Use lowercase letters for variable names. This is because Bash is case-sensitive, and using uppercase letters can cause errors in some cases.

- Avoid using reserved keywords or names that conflict with other variables or functions in the script. For example, do not use echo or if as variable names.

- Use meaningful prefixes to distinguish between variables with similar names. For example, use input_file and output_file to distinguish between variables that represent input and output files.

- Be consistent in your naming conventions. This will make it easier to read and understand your code.

By following these best practices, you can make your Bash scripts more readable and easier to maintain. In the next lesson, we will cover loops and conditional statements in Bash.

## Easy Assignments

1. Write a Bash script that declares a string variable called greeting and assigns it the value "Hello, world!". Print the value of the variable to the console.
2. Write a Bash script that declares two integer variables called x and y and assigns them the values 5 and 10, respectively. Calculate the sum of the variables and print the result to the console.
3. Write a Bash script that declares an array variable called fruits and assigns it the values "apple", "banana", and "orange". Print the second element of the array to the console.

## Medium Assignments

1. Write a Bash script that prompts the user to enter their name and stores the input in a variable called name. Use the echo command to print a personalized greeting that includes the user's name.
2. Write a Bash script that calculates the area of a rectangle based on the values of two integer variables length and width. Store the result in a variable called area and print the value to the console.
3. Write a Bash script that declares an array variable called numbers and assigns it the values 2, 4, 6, and 8. Use a loop to calculate the sum of the elements in the array and store the result in a variable called sum. Print the value of sum to the console.

## Hard Assignments

1. Write a Bash script that prompts the user to enter three integer values and stores them in variables a, b, and c. Use conditional statements to determine whether the sum of any two of the values is equal to the third value. If so, print a message to the console indicating which values satisfy this condition.
2. Write a Bash script that declares an array variable called names and assigns it the values "Alice", "Bob", "Charlie", and "Dave". Use a loop to prompt the user to enter their name. If the user's name is found in the names array, print a message to the console indicating that the user is on the list. If the user's name is not found, print a message indicating that the user is not on the list.
3. Write a Bash script that declares an array variable called grades and assigns it the values 75, 85, 92, and 68. Use a loop to calculate the average of the elements in the array and store the result in a variable called average. Then use conditional statements to determine the letter grade corresponding to the average, according to the following scale: 90-100 = A, 80-89 = B, 70-79 = C, 60-69 = D, below 60 = F. Print the letter grade to the console.