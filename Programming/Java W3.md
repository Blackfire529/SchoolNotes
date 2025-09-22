	The name of the java file **must match** the class name. When saving the file, save it using the class name and add ".java" to the end of the filename.

	Every line of code that runs in Java must be inside a `class`. And the class name should always start with an uppercase first letter.

	**Note:** Java is case-sensitive: "MyClass" and "myclass" has different meaning.

	
```java
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}```
	**Note:** The curly braces `{}` marks the beginning and the end of a block of code.
	`System` is a built-in Java class that contains useful members, such as `out`, which is short for "output". The `println()` method, short for "print line", is used to print a value to the screen (or a file).
	Don't worry too much about how `System`, `out` and `println()` works. Just know that you need them together to print stuff to the screen.
	You should also note that each code statement must end with a semicolon (`;`).
# [Print Text](https://www.w3schools.com/java/java_output.asp)
	You learned from the previous chapter that you can use the ==`println()`== method to output values or print text in Java:
	Text must be wrapped inside double quotations marks `""`.
	If you forget the double quotes, an error occurs:
	There is also a ==`print()`== method, which is similar to ==`println()`==.The only difference is that it does not insert a new line at the end of the output:
	You can also use the ==`println()`== method to print numbers.However, unlike text, we don't put numbers inside double quotes:You can also perform mathematical calculations inside the `println()` method:

# [Java Comments](https://www.w3schools.com/java/java_comments.asp)
	Single-line comments start with two forward slashes (`//`).Any text between `//` and the end of the line is ignored by Java (will not be executed).
	Multi-line comments start with `/*` and ends with `*/`.Any text between `/*` and `*/` will be ignored by Java.

---

# [Java Variables](https://www.w3schools.com/java/java_variables.asp)
```java
type variableName = value;
```
	All Java **variables** must be **identified** with **unique names**.These unique names are called **identifiers**.Identifiers can be short names (like x and y) or more descriptive names (age, sum, totalVolume).
	**Note:** It is recommended to use descriptive names in order to create understandable and maintainable code:- Reserved words (like Java keywords, such as `int` or `boolean`) cannot be used as names
 - [[#Strings]] - stores text, such as "Hello". String values are surrounded by double quotes
 - `int` - stores integers (whole numbers), without decimals, such as 123 or -123
- `float` - stores floating point numbers, with decimals, such as 19.99 or -19.99
- `char` - stores single characters, such as 'a' or 'B'. Char values are surrounded by single quotes
- `boolean` - stores values with two states: true or false
- `double`Stores fractional numbers. Sufficient for storing 15 to 16 decimal digits
- `long`Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
- `short`Stores whole numbers from -32,768 to 32,767

	if you don't want others (or yourself) to overwrite existing values, use the `final` keyword (this will declare the variable as "final" or "constant", which means unchangeable and read-only):The `final` keyword is called a "modifier".
	```java
final int myNum = 15;
myNum = 20;  // will generate an error: cannot assign a value to a final variable
```
### Declare Many Variables
Instead of writing:
```java
int x = 5;
int y = 6;
int z = 50;
System.out.println(x + y + z);
```
You can simply write:
```java
int x = 5, y = 6, z = 50;
System.out.println(x + y + z);
```
### One Value to Multiple Variables
```java
int x, y, z;
x = y = z = 50;
System.out.println(x + y + z);
```
# [Non-Primitive Data Types](https://www.w3schools.com/java/java_data_types_non-prim.asp)
	Non-primitive data types are called **reference types** because they refer to objects.
The main differences between **primitive** and **non-primitive** data types are:

- Primitive types in Java are predefined and built into the language, while non-primitive types are created by the programmer (except for `String`).
- Non-primitive types can be used to call methods to perform certain operations, whereas primitive types cannot.
- Primitive types start with a lowercase letter (like `int`), while non-primitive types typically starts with an uppercase letter (like `String`).
- Primitive types always hold a value, whereas non-primitive types can be `null`.

Examples of non-primitive types are [Strings](https://www.w3schools.com/java/java_strings.asp), [Arrays](https://www.w3schools.com/java/java_arrays.asp), [Classes](https://www.w3schools.com/java/java_classes.asp) etc.
## Java Type Casting
	Type casting is when you assign a value of one primitive data type to another type.

In Java, there are two types of casting:

- **Widening Casting** (automatically) - converting a smaller type to a larger type size  
    `byte` -> `short` -> `char` -> `int` -> `long` -> `float` -> `double`  
    Widening casting is done automatically when passing a smaller size type to a larger size type:
    ```java
public class Main {
  public static void main(String[] args) {
    int myInt = 9;
    double myDouble = myInt; // Automatic casting: int to double

    System.out.println(myInt);      // Outputs 9
    System.out.println(myDouble);   // Outputs 9.0
  }
}
```
    
- **Narrowing Casting** (manually) - converting a larger type to a smaller size type  
    `double` -> `float` -> `long` -> `int` -> `char` -> `short` -> `byte`
    Narrowing casting must be done manually by placing the type in parentheses `()` in front of the value:
    ```java
public class Main {
  public static void main(String[] args) {
    double myDouble = 9.78d;
    int myInt = (int) myDouble; // Manual casting: double to int

    System.out.println(myDouble);   // Outputs 9.78
    System.out.println(myInt);      // Outputs 9
  }
}
```

---

# Java Operators
### Arithmetic Operators

| Operator | Name           | Description                            | Example | Try it                                                                         |
| -------- | -------------- | -------------------------------------- | ------- | ------------------------------------------------------------------------------ |
| +        | Addition       | Adds together two values               | x + y   | [Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_add)  |
| -        | Subtraction    | Subtracts one value from another       | x - y   | [Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_sub)  |
| *        | Multiplication | Multiplies two values                  | x * y   | [Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_mult) |
| /        | Division       | Divides one value by another           | x / y   | [Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_div)  |
| %        | Modulus        | Returns the division remainder         | x % y   | [Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_mod)  |
| ++       | Increment      | Increases the value of a variable by 1 | ++x     | [Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_inc)  |
| --       | Decrement      | Decreases the value of a variable by 1 | --x     | [Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_dec)  |
### Assignment Operators
|Operator|Example|Same As|Try it|
|---|---|---|---|
|=|x = 5|x = 5|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_ass1)|
|+=|x += 3|x = x + 3|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_ass2)|
|-=|x -= 3|x = x - 3|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_ass3)|
|*=|x *= 3|x = x * 3|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_ass4)|
|/=|x /= 3|x = x / 3|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_ass5)|
|%=|x %= 3|x = x % 3|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_ass6)|
|&=|x &= 3|x = x & 3|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_ass7)|
|\|=|x \|= 3|x = x \| 3|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_ass8)|
|^=|x ^= 3|x = x ^ 3|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_ass9)|
|>>=|x >>= 3|x = x >> 3|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_ass10)|
|<<=|x <<= 3|x = x << 3|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_ass11)|
### Comparison Operators
|Operator|Name|Example|Try it|
|---|---|---|---|
|==|Equal to|x == y|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_compare1)|
|!=|Not equal|x != y|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_compare2)|
|>|Greater than|x > y|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_compare3)|
|<|Less than|x < y|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_compare4)|
|>=|Greater than or equal to|x >= y|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_compare5)|
|<=|Less than or equal to|x <= y|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_compare6)|
### Logical Operators
|Operator|Name|Description|Example|Try it|
|---|---|---|---|---|
|&&|Logical and|Returns true if both statements are true|x < 5 &&  x < 10|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_logical1)|
|\||Logical or|Returns true if one of the statements is true|x < 5 \| x < 4|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_logical2)|
|!|Logical not|Reverse the result, returns false if the result is true|!(x < 5 && x < 10)|[Try it »](https://www.w3schools.com/java/tryjava.asp?filename=demo_oper_logical3)|

---

# [Java Math](https://www.w3schools.com/java/java_math.asp)
	The Java Math class has many methods that allows you to perform mathematical tasks on numbers.

- The `Math.max(_x_,_y_)` method can be used to find the highest value of _x_ and _y_:
- The `Math.min(_x_,_y_)` method can be used to find the lowest value of _x_ and _y_:
- The `Math.sqrt(_x_)` method returns the square root of _x_:
- The `Math.abs(_x_)` method returns the absolute (positive) value of _x_:
- `Math.random()` returns a random number between 0.0 (inclusive), and 1.0 (exclusive):

---
# [Java If ... Else](https://www.w3schools.com/java/java_conditions.asp)
- Less than: a < b
- Less than or equal to: a <= b
- Greater than: a > b
- Greater than or equal to: a >= b
- Equal to a == b
- Not Equal to: a != b
- Use `if` to specify a block of code to be executed, if a specified condition is true
```java
if (condition) {
  // block of code to be executed if the condition is true
}
```
- Use [`else`](https://www.w3schools.com/java/java_conditions_else.asp) to specify a block of code to be executed, if the same condition is false
```java
if (condition) {
  // block of code to be executed if the condition is true
} else {
  // block of code to be executed if the condition is false
}
```
- Use [`else if`](https://www.w3schools.com/java/java_conditions_elseif.asp) to specify a new condition to test, if the first condition is false
```java
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}
```
- Use [`switch`](https://www.w3schools.com/java/java_switch.asp) to specify many alternative blocks of code to be executed
```java
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```
## The break Keyword

	When Java reaches a `break` keyword, it breaks out of the switch block.
	This will stop the execution of more code and case testing inside the block.
	When a match is found, and the job is done, it's time for a break. There is no need for more testing.
## The default Keyword

	The `default` keyword specifies some code to run if there is no case match:

## The Continue Keyword

	The `continue` statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.

---
# [While Loop](https://www.w3schools.com/java/java_while_loop.asp)
```java
while (condition) {
  // code block to be executed
}
```
**Note:** Do not forget to increase the variable used in the condition (`i++`), otherwise the loop will never end!
#### Do/While Loop
```java
do {
  // code block to be executed
}
while (condition);
```
	The `do/while` loop is a variant of the `while` loop. This loop will execute the code block **once**, before checking if the condition is true. Then it will repeat the loop as long as the condition is true.
	
**Note:** The semicolon `;` after the `while` condition is required!

	 The `do/while` loop always runs at least once, even if the condition is already false. This is different from a regular `while` loop, which would skip the loop entirely if the condition is false at the start. This behavior makes `do/while` useful when you want to ensure something happens at least once, like showing a message or asking for user input.

---
# [For Loop](https://www.w3schools.com/java/java_for_loop.asp)
```java
for (statement 1; statement 2; statement 3) {
  // code block to be executed
}
```
	Statement 1 is executed (one time) before the execution of the code block.
	Statement 2 defines the condition for executing the code block.
	Statement 3 is executed (every time) after the code block has been executed.

### for-each Loop
```java
for (type variableName : arrayName) {
  // code block to be executed
}
```
There is also a "**for-each**" loop, which is used exclusively to loop through elements in an [**array**](https://www.w3schools.com/java/java_arrays.asp) (or other [data structures](https://www.w3schools.com/java/java_data_structures.asp)):

---
# [Arrays](https://www.w3schools.com/java/java_arrays.asp)
	Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.
To declare an array, define the variable type with **square brackets**:
```java
String[] cars;
```
 To insert values to it, you can place the values in a comma-separated list, inside curly braces:
 ```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
```
To create an array of integers, you could write:
```java
int[] myNum = {10, 20, 30, 40};
```

## Access the Elements of an Array

You can access an array element by referring to the index number.
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars[0]);
// Outputs Volvo
```

To change the value of a specific element, refer to the index number:
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
cars[0] = "Opel";
System.out.println(cars[0]);
// Now outputs Opel instead of Volvo
```

To find out how many elements an array has, use the `length` property:
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars.length);
// Outputs 4
```
## [Multidimensional Arrays](https://www.w3schools.com/java/java_arrays_multi.asp)
	A multidimensional array is an array of arrays.
	Multidimensional arrays are useful when you want to store data as a tabular form, like a table with rows and columns.
To create a two-dimensional array, add each array within its own set of **curly braces**:
```java
int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
```

To access the elements of the **myNumbers** array, specify two indexes: one for the array, and one for the element inside that array. This example accesses the third element (2) in the second array (1) of myNumbers:
```java
int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
System.out.println(myNumbers[1][2]); // Outputs 7
```
**Remember that:** Array indexes start with 0: [0] is the first element. [1] is the second element, etc.

---
# [Methods/Functions](https://www.w3schools.com/java/java_methods.asp)
	A **method** is a block of code which only runs when it is called.You can pass data, known as parameters, into a method.Why use methods? To reuse code: define the code once, and use it many times.

A method must be declared within a class. It is defined with the name of the method, followed by parentheses **()**.
```java
public class Main {
  static void myMethod() {
    // code to be executed
  }
}
```

To call a method in Java, write the method's name followed by two parentheses **()** and a semicolon **;**
### Parameters and Arguments
	Information can be passed to methods as a parameter. Parameters act as variables inside the method.

Parameters are specified after the method name, inside the parentheses. You can add as many parameters as you want, just separate them with a comma. You can have as many parameters as you like:
```java
public class Main {
  static void myMethod(String fname, int age) {
    System.out.println(fname + " is " + age);
  }

  public static void main(String[] args) {
    myMethod("Liam", 5);
    myMethod("Jenny", 8);
    myMethod("Anja", 31);
  }
}

// Liam is 5
// Jenny is 8
// Anja is 31
```
**Note** that when you are working with multiple parameters, the method call must have the same number of arguments as there are parameters, and the arguments must be passed in the same order.
### Return Values
the `void` keyword indicates that the method should not return a value.
If you want the method to return a value, you can use a primitive data type (such as `int`, `char`, etc.) instead of `void`, and use the `return` keyword inside the method:
```java
public class Main {
  static int myMethod(int x) {
    return 5 + x;
  }

  public static void main(String[] args) {
    System.out.println(myMethod(3));
  }
}
// Outputs 8 (5 + 3)
```

```java
public class Main {
  static int myMethod(int x, int y) {
    return x + y;
  }

  public static void main(String[] args) {
    System.out.println(myMethod(5, 3));
  }
}
// Outputs 8 (5 + 3)
```

You can also store the result in a variable (recommended, as it is easier to read and maintain):
```java
public class Main {
  static int myMethod(int x, int y) {
    return x + y;
  }

  public static void main(String[] args) {
    int z = myMethod(5, 3);
    System.out.println(z);
  }
}
// Outputs 8 (5 + 3)
```
## Method Overloading
	With **method overloading**, multiple methods can have the same name with different parameters:
```java
int myMethod(int x)
float myMethod(float x)
double myMethod(double x, double y)
```

The following example has two methods that add numbers of different type:
```java
static int plusMethodInt(int x, int y) {
  return x + y;
}

static double plusMethodDouble(double x, double y) {
  return x + y;
}

public static void main(String[] args) {
  int myNum1 = plusMethodInt(8, 5);
  double myNum2 = plusMethodDouble(4.3, 6.26);
  System.out.println("int: " + myNum1);
  System.out.println("double: " + myNum2);
}
```
Instead of defining two methods that should do the same thing, it is better to overload one.
```java
static int plusMethod(int x, int y) {
  return x + y;
}

static double plusMethod(double x, double y) {
  return x + y;
}

public static void main(String[] args) {
  int myNum1 = plusMethod(8, 5);
  double myNum2 = plusMethod(4.3, 6.26);
  System.out.println("int: " + myNum1);
  System.out.println("double: " + myNum2);
}
```
**Note:** Multiple methods can have the same name as long as the number and/or type of parameters are different.
# Scope
In Java, variables are only accessible inside the region they are created. This is called **scope**.

Variables declared directly inside a method are available anywhere in the method following the line of code in which they were declared:
```java
public class Main {
  public static void main(String[] args) {

    // Code here CANNOT use x

    int x = 100;

    // Code here can use x
    System.out.println(x);
  
```
## Block Scope
	A block of code refers to all of the code between curly braces `{}`.

Variables declared inside blocks of code are only accessible by the code between the curly braces, which follows the line in which the variable was declared:
```java
public class Main {
  public static void main(String[] args) {

    // Code here CANNOT use x

    { // This is a block

      // Code here CANNOT use x

      int x = 100;

      // Code here CAN use x
      System.out.println(x);

    } // The block ends here

  // Code here CANNOT use x

  }
}
```
A block of code may exist on its own or it can belong to an `if`, `while` or `for` statement. In the case of `for` statements, variables declared in the statement itself are also available inside the block's scope.

# [Recursion](https://www.w3schools.com/java/java_recursion.asp)
Recursion is the technique of making a function call itself. This technique provides a way to break complicated problems down into simple problems which are easier to solve.
EX:Use recursion to add all of the numbers up to 10.
```java
public class Main {
	public static void main(String[] args) {
	    int result = sum(10);
	    System.out.println(result);
	}
	public static int sum(int k) {     
		if (k > 0) {
			return k + sum(k - 1);
		} else {       
			return 0;
    }
  }
}
```
Just as loops can run into the problem of infinite looping, recursive functions can run into the problem of infinite recursion. Infinite recursion is when the function never stops calling itself. Every recursive function should have a halting condition, which is the condition where the function stops calling itself. In the previous example, the halting condition is when the parameter `k` becomes 0.
The developer should be very careful with recursion as it can be quite easy to slip into writing a function which never terminates, or one that uses excess amounts of memory or processor power. However, when written correctly recursion can be a very efficient and mathematically-elegant approach to programming.

---
# [Classes/Objects](https://www.w3schools.com/java/java_classes.asp)
	Everything in Java is associated with classes and objects, along with its attributes and methods. For example: in real life, a car is an object. The car has **attributes**, such as weight and color, and **methods**, such as drive and brake.

### Create a Class
A Class is like an object constructor, or a "blueprint" for creating objects. To create a class, use the keyword class:
```java
public class Main {
  int x = 5;
}
```

### Create an Object
	In Java, an object is created from a class. 
We have already created the class named `Main`, so now we can use this to create objects. To create an object of `Main`, specify the class name, followed by the object name, and use the keyword `new`:
```java
public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj.x);
  }
}
```

You can create multiple objects of one class:
```java
public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj1 = new Main();  // Object 1
    Main myObj2 = new Main();  // Object 2
    System.out.println(myObj1.x);
    System.out.println(myObj2.x);
  }
}
```

If you create multiple objects of one class, you can change the attribute values in one object, without affecting the attribute values in the other:
Change the value of `x` to 25 in `myObj2`, and leave `x` in `myObj1` unchanged:
```java
public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj1 = new Main();  // Object 1
    Main myObj2 = new Main();  // Object 2
    myObj2.x = 25;
    System.out.println(myObj1.x);  // Outputs 5
    System.out.println(myObj2.x);  // Outputs 25
  }
}
```
# [Class Methods](https://www.w3schools.com/java/java_class_methods.asp)
	Methods are declared within a class, and that they are used to perform certain actions:
```java
public class Main {
  static void myMethod() {
    System.out.println("Hello World!");
  }

  public static void main(String[] args) {
    myMethod();
  }
}

// Outputs "Hello World!"
```
`myMethod()` prints a text (the action), when it is **called**. To call a method, write the method's name followed by two parentheses **()** and a semicolon **;**

## Static vs. Public
	You will often see Java programs that have either `static` or `public` attributes and methods.
**static** method - it can be accessed without creating an object of the class.
**public** method - it can only be accessed by objects:

# [Java Constructors](https://www.w3schools.com/java/java_constructors.asp)
	A constructor in Java is a **special method** that is used to initialize objects. The constructor is called when an object of a class is created. It can be used to set initial values for object attributes:
```java
// Create a Main class
public class Main {
  int x;  // Create a class attribute

  // Create a class constructor for the Main class
  public Main() {
    x = 5;  // Set the initial value for the class attribute x
  }

  public static void main(String[] args) {
    Main myObj = new Main(); // Create an object of class Main (This will call the constructor)
    System.out.println(myObj.x); // Print the value of x
  }
}

// Outputs 5
```
	Note that the constructor name must **match the class name**, and it cannot have a **return type** (like `void`).
	Also note that the constructor is called when the object is created. All classes have constructors by default: if you do not create a class constructor yourself, Java creates one for you. However, then you are not able to set initial values for object attributes.

## Constructor Parameters
	Constructors can also take parameters, which is used to initialize attributes.
```java
public class Main {
  int x;

  public Main(int y) {
    x = y;
  }

  public static void main(String[] args) {
    Main myObj = new Main(5);
    System.out.println(myObj.x);
  }
}

// Outputs 5
```
You can have as many parameters as you want:
```java
public class Main {
  int modelYear;
  String modelName;

public Main(int year, String name) {
    modelYear = year;
    modelName = name;
}

public static void main(String[] args) {
    Main myCar = new Main(1969, "Mustang");
	    System.out.println(myCar.modelYear + " " + 
	    myCar.modelName);
	}
}

// Outputs 1969 Mustang
```
## [this Keyword](https://www.w3schools.com/java/java_this.asp)
	The `this` keyword in Java refers to the current object in a method or constructor. The `this` keyword is often used to avoid confusion when class attributes have the same name as method or constructor parameters.

Sometimes a constructor or method has a parameter with the same name as a class variable. When this happens, the parameter temporarily **hides** the class variable inside that method or constructor. To refer to the class variable and not the parameter, you can use the `this` keyword:
```java
public class Main {
	int x;  // Class variable x

  // Constructor with one parameter x
	public Main(int x) {
	    this.x = x; // refers to the class variable x
	}

	public static void main(String[] args) {
		// Create an object of Main and pass the value 5 to the constructor
	    Main myObj = new Main(5);
	    System.out.println("Value of x = " + myObj.x);
	}
}
// Output: Value of x = 5
```

You can also use `this()` to call another constructor in the same class. This is useful when you want to provide default values or reuse initialization code instead of repeating it.
```java
public class Main {
  int modelYear;
  String modelName;

  // Constructor with one parameter
  public Main(String modelName) {
    // Call the two-parameter constructor to reuse code and set a default year    
    this(2020, modelName);
  }

  // Constructor with two parameters
  public Main(int modelYear, String modelName) {
    // Use 'this' to assign values to the class variables
    this.modelYear = modelYear;
    this.modelName = modelName;
  }

  // Method to print car information
  public void printInfo() {
    System.out.println(modelYear + " " + modelName);
  }

  public static void main(String[] args) {
    // Create a car with only model name (uses default year)
    Main car1 = new Main("Corvette");

    // Create a car with both model year and name
    Main car2 = new Main(1969, "Mustang");

    car1.printInfo();
    car2.printInfo();
  }
}
```
**Note:** The call to `this()` must be the **first statement** inside the constructor.
### When to use this?
- When a constructor or method has a parameter with the same name as a class variable, use **`this`** to update the class variable correctly.
- To call another constructor in the same class and reuse code.