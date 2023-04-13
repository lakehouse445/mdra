# MedoraScript (mdra)

MedoraScript (mdra) is a programming language inspired by the town of Medora, North Dakota. All lines must start with the keyword `in_medora_mode;`. The language supports basic programming constructs such as variables, loops, conditionals, functions, and input/output operations, with a unique Medora twist.

## Syntax

Here's a summary of the syntax for the main elements of MedoraScript:

- Variables: `in_medora_mode;mdra_var(name, value);`
- Constants: `in_medora_mode;mdra_const(name, value);`
- Conditionals: `in_medora_mode;mdra_if(condition);`, `in_medora_mode;mdra_elif(condition);`, `in_medora_mode;mdra_else();`, `in_medora_mode;mdra_endif();`
- Loops: `in_medora_mode;mdra_for(init, condition, increment);`, `in_medora_mode;mdra_while(condition);`, `in_medora_mode;mdra_endloop();`
- Functions: `in_medora_mode;mdra_def(func_name, args);`, `in_medora_mode;mdra_enddef();`, `in_medora_mode;mdra_call(func_name, args);`
- Input: `in_medora_mode;mdra_input(prompt);`
- Output: `in_medora_mode;mdra_print(message);`
- Comments: `in_medora_mode;mdra_comment(content);`
- Lists: `in_medora_mode;mdra_list(name, elements);`, `in_medora_mode;mdra_list_append(name, element);`, `in_medora_mode;mdra_list_remove(name, index);`, `in_medora_mode;mdra_list_length(name);`

## Example Program

Here's an example program in MedoraScript that calculates the Fibonacci sequence up to a given number of terms entered by the user:

```mdra
in_medora_mode;mdra_var(terms, 0);
in_medora_mode;mdra_var(first, 0);
in_medora_mode;mdra_var(second, 1);
in_medora_mode;mdra_var(temp, 0);
in_medora_mode;mdra_var(counter, 1);

in_medora_mode;mdra_print("Enter the number of terms for the Fibonacci sequence:");
in_medora_mode;mdra_input(terms);

in_medora_mode;mdra_if(terms == 0);
    in_medora_mode;mdra_print("Please enter a positive integer.");
    in_medora_mode;mdra_endif();

in_medora_mode;mdra_elif(terms == 1);
    in_medora_mode;mdra_print("Fibonacci sequence up to 1 term:");
    in_medora_mode;mdra_print(first);
    in_medora_mode;mdra_endif();

in_medora_mode;mdra_else();
    in_medora_mode;mdra_print("Fibonacci sequence up to " + terms + " terms:");
    in_medora_mode;mdra_print(first);
    in_medora_mode;mdra_print(second);

    in_medora_mode;mdra_while(counter < terms - 1);
        in_medora_mode;mdra_var(temp, first + second);
        in_medora_mode;mdra_print(temp);
        in_medora_mode;mdra_var(first, second);
        in_medora_mode;mdra_var(second, temp);
        in_medora_mode;mdra_var(counter, counter + 1);
        in_medora_mode;mdra_endloop();

    in_medora_mode;mdra_endif();
```
## Output

For an input of 7, the output would be:

```Enter the number of terms for the Fibonacci sequence:
Fibonacci sequence up to 7 terms:
0
1
1
2
3
5
8
```

This example demonstrates the use of variables, input/output, conditionals, and loops in MedoraScript. You can build more complex programs by combining these constructs and utilizing user-defined functions and built-in functions.
