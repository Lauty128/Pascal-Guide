# **PASCAL GUIDE**

This is a structured language, so pascal uses a **strict** way of work. 


## STRUCTURE

Now let's see at the pascal structure
```pascal
program nameProgram;

Uses
    { library list };

Type
    { data type list };

Procedure name( { parameters} );
Begin
    //code of the procedure 
End;

Function name( { parameters} ):type;
Begin
    //code of the function
End;

Var
  { variables list };

Begin
  // main program code        
End.
```

>* This is the order of the main program 
>* Only the procedure and the function can be changed between them. The others do not move


## VARIABLE DECLARATIONS

### **Var**
The variables are used to store data inside a program.\
Let's see an example:

```pascal
Var nombre:String;  // Variable of type String
    edad:Integer;  //  Variable of type Integer
```

 Are declared as follows.\
 You can declare more than one variable of the same Type in a line of code, separating each variable with a ","

```pascal
Var nombre,apellido,localidad:String;  
```

### **Assignments**
You can assign a value to the variable when you declared it 
```pascal
Var edad:Integer = 5;  
```
> This only works with global variables

### **Type**
This is mainly used to declare arrays and records.
```pascal
Type
  libros = record
    id: Integer;
    titulo: String;
    autor: String;
  End;
  dias = array[1..7] of Integer;

```
> Are declared differently from the variables (=)

then, to call it we do the following
```pascal
Var
    variable1:dias;
    variable2:libros;
```


## COMMENTS
There are 3 ways to write a comment 
```pascal
    { comment one }
    (* comment two *)
    // comment three
```
> The last comment uses the whole line. From "//" onwards 

## INPUT/OUTPUT
To handle pascal inputs and outputs we use two functions 
```pascal
    Readln({Var})  
    //The program allows you to write the value of the variable

    WriteLn({text or Var}) 
    //The program prints the variable or text on the screen
```
> you must use the corresponding data type in each case

## TYPES OF DATA
There are several types of data, but let's see the most basic ones

| Type        | Example
|-------------|----------
| **Integer** | 5
| **Real**    | 3.45
| **String**  | 'text string'
| **Char**    | 'h'
| **Boolean** | *true* or *false* 

## OPERATORS

### **Relational**

| Meaning      | Operator |      
|--------------|----------|      
| Mayor        |    >     |      
| Menor        |    <     |      
| Igual        |    =     |      
| Menor o Igual|    <=    |      
| Mayor o Igual|    >=    |      
| Distinto     |    <>    |      

### **Logics**
| Meaning      | Operator |      
|--------------|----------|      
| And          | **and**  |      
| Or           | **or**   |      
| Not          | **not**  |

**and**: both operators must be complied\
**or**: at least one must be complied \
**not**: inverts the value of the operator

### **Mathematicians**
| Meaning          | Operator | Parameters    |
|------------------|----------|---------------|  
| Sum              | +        | Real, Integer |
| Subtract         | -        | Real, Integer |
| Multiply         | *        | Real, Integer |
| Division         | /        | Real, Integer |
| Integer Division | **div**  | Integer       |
| Module           | **mod**  | Integer       |

## CONDITIONALS
```pascal
    if(logical expression) then
        Begin
            // Code A
        End
    else
        Begin
            // Code B
        End;
```
if the logical expression is true, then it will execute the code A, else the code B
>* if the condicional does not end, then you must not put ";" at the finish
>* if the code is one line, then it isn't required the **begin** and **end**
```pascal
    if(logical expression) then
        // one line code
    else
        Begin
            // Code
        End;
```

### **SENTENCE FOR**
allows us to repeat a code as many times as we want
```pascal
    for {var}:=initial-value to final-value do
      Begin
        // Code
      End;
```
we can put that the variable "i" starts at 1 and ends at 5.
Then the code is repeat until all laps are completed

### **WHILE**
With this we can repeat a block of code as many times as we want, as long as the condition is met.
```pascal
    While { condition } Do
      Begin
        // Code
      End;
```

## POCEDURES & FUNCTIONS
A function is equal to a procedure. the only diffence is that a function returns a simple value
### **Procedure**
```pascal
    Procedure name({var}:{type}; {var}:{type});
    var {local-var}:{type};
      Begin
        // Code
      End;
```
>* first goes the parameters with their data type
>* after, if you want to use local variables, we use ```var``` to declare them 
>* if the parameter contains the word "var" before its name, then the global variable enters as a reference

### **Function**
This is very similar to the procedure, with the difference that the function return something.
```pascal
    Function name({var}:{type}; {var}:{type}):type;
    var {local-var}:{type};
      Begin
        // Code
        name:= { something of the specified data type } ;
      End;
```
>* No parameter enters as reference
>* At the end we must put a value to the function { ``` name:= ``` }
>* the function value must be of the specified data type


## Records & Arrays
Together, these are used to store data and keep them organized.
it Is recommended to declare them in ```Type```
```pascal
  Type
    registro= Record
      nombre:String;
      edad:Integer;
      localidad:String;
    End;
    arreglo= Array[1..5] of registro;
```
>* Remember that **types** are declared with  ```=```
>* the array goes from **1** to **5** and is of type ```registro```

### **Call them in the main program**
To do so, they must be declared in ```Var``` and later in the main program
```pascal
  Var
    datos: arreglo;
    i:Integer;

  Begin
    For i:=1 to 5 do
    Begin
      Readln(datos[i].nombre); //String
      Readln(datos[i].edad); //Integer
      Readln(datos[i].localidad); //String
    End;

    //Writeln(datos)
    //Writeln(datos[1])
    Writeln(datos[1].nombre)

  End.
```
>* Those ```Writeln()``` commented cannot be executed by Pascal. Must be printed in this way - **One by one**
>* Variables must be declared with  ```:```

This program, loads ```datos``` and the records it contains
