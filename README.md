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
  dias = array[1..7] of Integer;
  libros = record
    id: Integer;
    titulo: String;
    autor: String;

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
