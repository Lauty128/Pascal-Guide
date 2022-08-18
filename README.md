# **PASCAL GUIDE**

This is a structured language, so pascal uses a **strict** way of work. 


## ESTRUCTURE

Now let's see at the pascal structure
```pascal
program nameProgram;

Uses
    { library list };

Type
    { data type list };

Procedure name();
Begin
    //procedure's code
End;

Function name():type;
Begin
    //function's code
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
let's see an example:

```pascal
Var nombre:String;  // Variable of type String
    edad:Integer;  //  Variable of type Integer
```

 Are declared as follows.\
 you can declare more than one variable of the same type in a line of code, separating each variable with a ","

```pascal
Var nombre,apellido,localidad:String;  
```

### **Assignments**
you can assign a value to the variable when you declared it 
```pascal
Var edad:Integer = 5;  
```
> This only works with global variables, no with local variables

### **Type**
This is mainly used to declared arrays and records.
```pascal
Type
  dias = array[1..7] of Integer;
  libros = record
    id: Integer;
    titulo: String;
    autor: String;

```
> Are declared differently from the variables 

then, to call it we do the following
```pascal
Var
    variable1:dias;
    variable2:libros;
```