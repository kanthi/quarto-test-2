# variables

Bash variables are named containers for storing data values. They are used to store information that needs to be referenced or modified during the execution of a script.

## Declaring Variables

To declare a variable in Bash, you can use the `declare` command followed by the variable name and its value:

```bash
declare variable_name=value
```

For example:

```bash
declare my_variable="Hello, World!"
```

## Accessing Variables

You can access the value of a variable by using the variable name:

```bash
echo $my_variable
```

## Modifying Variables

You can modify the value of a variable by assigning a new value to it:

```bash
my_variable="Goodbye, World!"
```

## Removing Variables

You can remove a variable by using the `unset` command:

```bash
unset my_variable
```

## Scope of Variables

Variables declared inside a function have local scope, while variables declared at the top level have global scope.

## Exporting Variables

You can export a variable by using the `export` command:

```bash
export my_variable
```

This allows you to access the variable from other scripts or programs.

## Passing Arguments to a Script

You can pass arguments to a script by using the `$1`, `$2`, etc. variables. These variables contain the first, second, etc. arguments passed to the script when it is executed.

```bash
./script.sh arg1 arg2 arg3
```

## Getting the Number of Arguments Passed to a Script

You can get the number of arguments passed to a script by using the `$#` variable:

```bash
echo "Number of arguments: $#"
```

## Getting the Name of the Script

You can get the name of the script by using the `$0` variable:

```bash
echo "Script name: $0"
```

## Getting the Current Working Directory

You can get the current working directory by using the `$PWD` variable:

```bash
echo "Current working directory: $PWD"
```

## Getting the Home Directory

You can get the home directory by using the `$HOME` variable:

```bash
echo "Home directory: $HOME"
```

## Getting the User Name

You can get the user name by using the `$USER` variable:

```bash
echo "User name: $USER"
```



