```c
#include <stdio.h>
#include <conio.h>

void add();

int main(){
    add();
    getch();
}

void add(){
    int n1, n2, result;
    printf("enter any 2 numbers\n");
    scanf("%d%d",&n1,&n2);
    result=n1+n2;
    printf("sum of two numbers is %d\n", result);
}
```

```c
#include <stdio.h>
#include <conio.h>

void add();

int main(){
    add();
    getch();
}

void add(){
    int i;
    for(i=1;i<21;i++){
        printf("*");
    }

printf("\n");
printf(" | welcome to akgec ");
printf("\n");

for(i=1;i<21;i++){
    printf("*");
}

}
```

```c
#include <stdio.h>
#include <conio.h>

void add(int x, int y, int z,int u, int v);

int main(){

int a,b,c,d,e;
printf("enter no. a");
scanf("%d",&a);
printf("enter no. b");
scanf("%d",&b);
printf("enter no. c");
scanf("%d",&c);
printf("enter no. d");
scanf("%d",&d);
printf("enter no. e");
scanf("%d",&e);

add(a,b,c,d,e);

}

void add(int x, int y, int z,int u,int v){

int add;

add = x+y+z+u+v;

printf("add=%d",add);

}

```

```c

#include<stdio.h>
#include<conio.h>

void pal(int n);

void main(){
    int a;
    printf("\n Enter a no. ");
    scanf("%d",&a);
    pal(a);
}

void pal(int n){
    int m,d;
    int r=0;
    m=n;
    while(m>0){
        d=m%10;
        r=r*10+d;
        m=m/10;
        
    }
    if(n==r){
        printf("\n Palindrome no.");
        
    }
    else{
        printf("\n Not Palindrome no.");
        
    }

}
```

### reversing a number 
```c
#include<stdio.h>
#include<conio.h>

void rev();

void main(){
    rev();
    getch();
    
    return 0;
}

void rev(){
    int a;
    printf("\n Enter a no.");
    scanf("%d",&a);
    int m,d;
    int r=0;
    m=a;
    while(m>0){
        d=m%10;
        r=r*10+d;
        m=m/10;
    }
    printf("\n reverse no.=%d",r);
}
```

### factorial
```c
#include <stdio.h>
#include<conio.h>

int fac(int n);

void main(){
    int a;
    int m;
    printf("enter a");
    scanf("%d",&a);
    m=fac(a);
    printf("factorial =%d",m);
}

int fac(int n){
    int i;
    int f=1;
    for(i=1;i=n;i++){
       f*=i;
    }
    return(f);
}

}
```

### swapping numbers

```c
#include <stdio.h>
#include<conio.h>

void swap(int a, int b);

void main(){
    int a,b;
    printf("enter first no.");
    scanf("%d",&a);
    printf("enter second no.");
    scanf("%d",&b);
    swap(a,b); //actual parameter
    printf("main fun value of a is=%d",a);
    printf("main fun value of b is=%d",b);
}

void swap(int a, int b){
    int temp;
    temp = a;
    a=b;
    b=temp;
    printf("after swaping first no. =%d",a);
    printf("\n");
    printf("after swaping sec no. =%d",b);
}
```

### calculating age

```c
#include<stdio.h>
#define age(a,b) a-b

int main(){
    printf("your age =%d",age(2025,2006));
}
```

###  greatest number 

```c
#include<conio.h>
#include <stdio.h>

#define MAX(a,b) if(a>b) \
                    printf("%d is greater",a); \
                    else \
                    printf("%d is greater",b);
int main(){
    MAX(4,5);
    return 0;
}

```

### multiply 
```c
#include <stdio.h>
#define multi(a,b) (a)*(b)
#include <conio.h>

void main(){
    printf("%d",multi(10,20)+76);
    getch;
}
```


```c
#include<stdio.h>
#include<conio.h>

void main(){
    int i,j,n,k,temp,a[n];
    printf("enter size of elements");
    scanf("%d",&n);
    printf("enter elements of array");
    for(i=0;i<=n;i++){
        scanf("%d",&a[n]);
        
    }
    for(i=1;i<n;i++){
        temp=a[i];
        j=i-1;
        while(temp>=0 && a[j]>temp){
            a[j+1]=a[j];
            j--;
            
        }
    a[j+1]=temp;
    }
    for(i=0;i<=n;i++){
        printf("%d",a[k]);
        
    }

}

```

```c
#include<stdio.h>
#include<conio.h>

void main() {
    int i,j,n,temp;
    printf("enter size of elements");
    scanf("%d",&n);
    int a[n];
    printf("enter elements of array");
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    for(i=0;i<n-1;i++){
        for(j=0;j<n-1;j++){
            if(a[j]>a[j+1]){
                temp=a[j];
                a[j]=a[j+1];
                a[j+1]=temp;
            }
        }
        
    }
    for(i=0;i<n;i++){
        printf("%d",a[i]);
    }

}
```

```c

#include <stdio.h>
#include <conio.h>
#include <stdlib.h>

void main()
{
    int n;
    int i;
    int *ptr;
    int *pqr;

    printf("enter no. of values ");
    scanf("%d",&n);

    ptr = (int*) malloc(n * sizeof(int));
    pqr = ptr;

    printf("\n enter value =%d", n);
    for(i = 0; i < n; i++) {
        scanf("%d", ptr);
        ptr++;
    }

    ptr = pqr;
    printf("\n values are ");
    for(i = 0; i < n; i++) {
        printf("%d", *ptr);
        ptr++;
    }

    printf("\n enter new no. of values ");
    scanf("%d",&n);

    ptr = (int*) realloc(pqr, n * sizeof(int));
    pqr = ptr;

    printf("\n enter value =%d", n);
    for(i = 1; i <= n; i++) {
        scanf("%d", ptr);
        ptr++;
    }

    ptr = pqr;
    printf("your values are");
    for(i = 1; i <= n; i++) {
        printf("\n %d", *pqr);
        pqr++;
    }
}

```

```c
#include <stdio.h>
#include <string.h>

int isPalindrome (char str[]) {
    int start = 0;
    int end = strlen(str) -1;
    while (start < end) {
        if (str[start] != str[end]) {
            return 0; // Not a palindrome
        }
        start++;
        end--;
    }
    return 1; // Palindrome
}

int main() {
    char str[100];
    printf("Enter a string: ");
    scanf("%s", str);
    if (isPalindrome (str)) {
        printf("\%s\" is a palindrome. \n", str);
        
    } else {
        printf("\%s\" is not a palindrome. \n", str);
    }
    return 0;
}
```

```c
#include <stdio.h>
#include <conio.h>

struct code{
    int i;
    char c;
    struct code *ptr;
};

void main(){
    struct code var1;
    struct code var2;
    var1.i =55;
    var1.c ='A';
    var1.ptr=NULL;
    var2.i =66;
    var2.c = 'B';
    var1.ptr = &var2;
    printf("\n %d %c", var1.ptr->i,var1.ptr->c);
}
```

# Function-
Function type on return and argument 

Here are examples for all four cases:

---

### 1. **No Return, No Argument**
```c
#include <stdio.h>

// Function with no return and no arguments
void greet() {
    printf("Hello! Welcome to the program.\n");
}

int main() {
    greet(); // Call the function
    return 0;
}
```

**Output:**
```
Hello! Welcome to the program.
```

---

### 2. **No Return, But Argument**
```c
#include <stdio.h>

// Function with no return but with arguments
void displayNumber(int num) {
    printf("The number is: %d\n", num);
}

int main() {
    int n = 25;
    displayNumber(n); // Call the function and pass an argument
    return 0;
}
```

**Output:**
```
The number is: 25
```

---

### 3. **Return With Argument**
```c
#include <stdio.h>

// Function with return and arguments
int addNumbers(int a, int b) {
    return a + b; // Return the sum of the two numbers
}

int main() {
    int num1 = 10, num2 = 20;
    int sum = addNumbers(num1, num2); // Call the function and store the result
    printf("The sum is: %d\n", sum);
    return 0;
}
```

**Output:**
```
The sum is: 30
```

---

### 4. **Return Without Argument**
```c
#include <stdio.h>

// Function with return and no arguments
int getNumber() {
    return 42; // Return a fixed number
}

int main() {
    int num = getNumber(); // Call the function and store the result
    printf("The number is: %d\n", num);
    return 0;
}
```

**Output:**
```
The number is: 42
``` 

### Explanation of Each Case:
1. **No Return, No Argument**: The function doesn't return any value or take input.
2. **No Return, But Argument**: The function takes input but doesn't return any value.
3. **Return With Argument**: The function takes input and returns a result.
4. **Return Without Argument**: The function doesn't take input but returns a result.


# Pointers-
Pointers 

Here’s your code:
---
```c
#include<stdio.h>

int main() {
    int age = 22;

    int *ptr = &age;

    int _age = *ptr;

    printf("%d\n", _age);

    // Address
    printf("%p\n", &age);
    printf("%p\n", ptr);
    printf("%p\n", &ptr);

    // Data
    printf("%d\n", age);
    printf("%d\n", *ptr);
    printf("%d\n", *(&age));

    return 0;
}
```
output
22
garbage 
garbage 
garbage
22
22
22
Here is an example of a simple **call by value** program in C:

---

### Code:
```c
#include <stdio.h>

// Function to demonstrate call by value
void modifyValue(int num) {
    printf("Inside function (before modification): num = %d\n", num);
    num = 20; // Modify the value of the parameter
    printf("Inside function (after modification): num = %d\n", num);
}

int main() {
    int num = 10;

    printf("Before function call: num = %d\n", num);

    // Call the function
    modifyValue(num);

    printf("After function call: num = %d\n", num);

    return 0;
}
```

### Explanation:
1. **Call by Value**:
   - In call by value, the value of the variable is passed to the function.
   - The function creates a copy of the variable in its own memory space.
   - Any changes made to the variable inside the function do not affect the original variable.

2. **How It Works**:
   - In the `main()` function, the value of `num` is 10.
   - When the `modifyValue()` function is called, a copy of `num` is passed to the function.
   - Modifications inside `modifyValue()` do not affect the original `num` in `main()`.

### Output:
```
Before function call: num = 10
Inside function (before modification): num = 10
Inside function (after modification): num = 20
After function call: num = 10
```

Here is an example of a **call by reference** program in C using pointers:

### Code:
```c
#include <stdio.h>

// Function to demonstrate call by reference
void modifyValue(int *num) {
    printf("Inside function (before modification): *num = %d\n", *num);
    *num = 20; // Modify the value of the variable using the pointer
    printf("Inside function (after modification): *num = %d\n", *num);
}

int main() {
    int num = 10;

    printf("Before function call: num = %d\n", num);

    // Call the function and pass the address of num
    modifyValue(&num);

    printf("After function call: num = %d\n", num);

    return 0;
}
```

### Explanation:
1. **Call by Reference**:
   - In call by reference, the address of the variable is passed to the function.
   - The function uses the pointer to directly access and modify the original variable.

2. **How It Works**:
   - In the `main()` function, the variable `num` has an initial value of `10`.
   - The address of `num` is passed to the `modifyValue()` function.
   - Inside `modifyValue()`, the dereferenced pointer (`*num`) is used to modify the value of the original variable.

### Output:
```
Before function call: num = 10
Inside function (before modification): *num = 10
Inside function (after modification): *num = 20
After function call: num = 20
```

### Key Point:
- The value of `num` in the `main()` function is changed after the function call, demonstrating **call by reference**.

### Code Example 1: Passing Address by Value

```c
#include<stdio.h>

void printAddress(int n);

int main() {
    int n = 4;
    printAddress(n);
    printf("address of n in main is %p\n", (void*)&n);
    return 0;
}

void printAddress(int n) {
    printf("address of n in printAddress is %p\n", (void*)&n);
}
```

#### Output:
The memory addresses will be different because `n` is passed by value, and the function uses a new copy of the variable:
```
address of n in printAddress is 0x7ffeefbff58c
address of n in main is 0x7ffeefbff58e
```

---

### Code Example 2: Passing Address by Reference (Using Pointers)

```c
#include<stdio.h>

void printAddress(int *n);

int main() {
    int n = 4;
    printAddress(&n);
    printf("address of n in main is %p\n", (void*)&n);
    return 0;
}

void printAddress(int *n) {
    printf("address of n in printAddress is %p\n", (void*)n);
}
```

#### Output:
The memory addresses will be the same because the function receives the actual address of the variable:
```
address of n in printAddress is 0x7ffeefbff58c
address of n in main is 0x7ffeefbff58c
```

### Key Difference:
- In **Code Example 1**, the variable is passed by value, so a copy is created, and the addresses differ.
- In **Code Example 2**, the address is passed directly, so both functions refer to the same memory location.


# Nptel
Program in NPTEL  c programming 

 **c variable**:  

```c
#include <stdio.h>

// Global variable
int globalVar = 100;

// Function to demonstrate the use of static and automatic variables
void demonstrateVariables() {
    // Static variable (retains its value between function calls)
    static int staticVar = 10;
    
    // Automatic variable (lifetime limited to function scope)
    int autoVar = 5;

    printf("Inside demonstrateVariables function:\n");
    printf("Static Variable: %d\n", staticVar);
    printf("Automatic Variable: %d\n", autoVar);

    // Modify the variables
    staticVar++;
    autoVar++;
}

int main() {
    // Local variable (defined inside main function)
    int localVar = 20;

    printf("In main function:\n");
    printf("Global Variable: %d\n", globalVar);
    printf("Local Variable: %d\n", localVar);

    printf("\nCalling demonstrateVariables for the first time:\n");
    demonstrateVariables();

    printf("\nCalling demonstrateVariables for the second time:\n");
    demonstrateVariables();

    return 0;
}
```

### **Expected Output:**
```
In main function:
Global Variable: 100
Local Variable: 20

Calling demonstrateVariables for the first time:
Inside demonstrateVariables function:
Static Variable: 10
Automatic Variable: 5

Calling demonstrateVariables for the second time:
Inside demonstrateVariables function:
Static Variable: 11
Automatic Variable: 5
```

This code **correctly demonstrates**:
✔ **Global variables** (retain values across the whole program).  
✔ **Local variables** (exist only within their function).  
✔ **Static variables** (retain values between function calls).  
✔ **Automatic variables** (reinitialize every function call).  

---

### **C datatype:**
```c
#include <stdio.h>

int main() {
    // Integer data type
    int intVar = 10;

    // Floating-point data type
    float floatVar = 20.5f;

    // Double-precision floating-point data type
    double doubleVar = 30.123456;

    // Character data type
    char charVar = 'A';

    // String (character array)
    char stringVar[] = "Hello, C!";

    // Print the values and sizes of the variables
    printf("Integer:\n");
    printf(" Value: %d\n", intVar);
    printf(" Size: %lu bytes\n\n", sizeof(intVar));

    printf("Floating-point:\n");
    printf(" Value: %f\n", floatVar);
    printf(" Size: %lu bytes\n\n", sizeof(floatVar));

    printf("Double-precision Floating-point:\n");
    printf(" Value: %lf\n", doubleVar);
    printf(" Size: %lu bytes\n\n", sizeof(doubleVar));

    printf("Character:\n");
    printf(" Value: %c\n", charVar);
    printf(" Size: %lu bytes\n\n", sizeof(charVar));

    printf("String:\n");
    printf(" Value: %s\n", stringVar);
    printf(" Size: %lu bytes\n\n", sizeof(stringVar));

    return 0;
}
```

---

### **Expected Output:**
```
Integer:
 Value: 10
 Size: 4 bytes

Floating-point:
 Value: 20.500000
 Size: 4 bytes

Double-precision Floating-point:
 Value: 30.123456
 Size: 8 bytes

Character:
 Value: A
 Size: 1 byte

String:
 Value: Hello, C!
 Size: 10 bytes
```

### **Explanation:**
- **`sizeof(intVar)`** → Usually **4 bytes** (depends on system).
- **`sizeof(floatVar)`** → Usually **4 bytes**.
- **`sizeof(doubleVar)`** → Usually **8 bytes**.
- **`sizeof(charVar)`** → **1 byte** (as expected).
- **`sizeof(stringVar)`** → **Includes the null terminator (`\0`)**, making it **length + 1**.

---

### **C signed and unsigned variable:**
```c
#include <stdio.h>

int main() {
    // Declare signed and unsigned integers
    signed int signedVar = -100;  // Signed integer can hold negative values
    unsigned int unsignedVar = 100; // Unsigned integer can only hold non-negative values

    // Display the values of the signed and unsigned integers
    printf("Signed Integer: \n");
    printf(" Value: %d\n", signedVar);

    printf("Unsigned Integer: \n");
    printf(" Value: %u\n", unsignedVar);

    // Assigning a negative value to an unsigned integer
    unsigned int invalidUnsigned = -1;

    printf("Unsigned Integer with a negative assignment (-1):\n");
    printf(" Value: %u\n", invalidUnsigned); // Typically prints 4,294,967,295 on a 32-bit system

    return 0;
}
```

---

### **Expected Output (on a 32-bit system):**
```
Signed Integer: 
 Value:-100

Unsigned Integer: 
 Value: 100

Unsigned Integer with a negative assignment (-1):
 Value: 4294967295
```

### **Explanation:**
- **`signedVar = 100;`** → Holds positive and negative values.
- **`unsignedVar = 100;`** → Cannot hold negative values.
- **`invalidUnsigned = -1;`**  
  - Since `unsigned int` **cannot store negative values**, `-1` is stored as **the maximum possible unsigned integer**.
  - On a **32-bit system**, this results in **4,294,967,295 (2³² - 1)**.

Your corrected code now runs without errors and correctly demonstrates signed vs. unsigned integers. 🚀

Your code contains **syntax errors and incorrect assignment operations**. Below is a **corrected version** with explanations:

---

### **Key Fixes:**
1. **Fixed `printf()` Formatting Errors:**
   - `"Enter two integers (a and b): "` should be on a new line for clarity.
   - Closing quotes (`"`) were missing at the end of some `printf()` statements.

2. **Fixed `+=`, `-=`, and `*=` Operations:**
   - **`+= b;`** was incorrect (it should be `c += b;`).
   - **`c = b;`** was incorrectly placed (should use `c -= b;` and `c *= b;`).

3. **Ensured Proper Code Execution Order:**
   - **Each assignment modifies `c`, so it should be done sequentially.**

---

### **C operator:**
```c
#include <stdio.h>

int main() {
    int a, b, c;

    // Input two integers from the user
    printf("Enter two integers (a and b): ");
    scanf("%d %d", &a, &b);

    // Displaying assignment operations
    printf("\nAssignment Operations Results:\n");

    // Simple assignment
    c = a;
    printf("c = a: c = %d\n", c);

    // Add the value of b to c and assign the result to c
    c += b; // Equivalent to c = c + b
    printf("c += b: c = %d\n", c);

    // Subtract the value of b from c and assign the result to c
    c -= b; // Equivalent to c = c - b
    printf("c -= b: c = %d\n", c);

    // Multiply c by b and assign the result to c
    c *= b; // Equivalent to c = c * b
    printf("c *= b: c = %d\n", c);

    return 0;
}
```

---

### **Expected Output (Example Run):**
```
Enter two integers (a and b): 5 3

Assignment Operations Results:
c = a: c = 5
c += b: c = 8
c -= b: c = 5
c *= b: c = 15
```

---

### **Explanation of Assignment Operators:**
1. **`c = a;`** → Assigns `a` to `c`.  
2. **`c += b;`** → `c = c + b` (adds `b` to `c`).  
3. **`c -= b;`** → `c = c - b` (subtracts `b` from `c`).  
4. **`c *= b;`** → `c = c * b` (multiplies `c` by `b`).  

Your code is **almost correct**, but there's a small issue with the format specifier. `%s` is used for strings, but `"true"` and `"false"` are string literals. This works in modern compilers but is not strictly type-safe in standard C.  

---

### **Key Fixes:**
1. **Using `"true"` and `"false"` safely**:
   - Instead of `%s`, we can use **`printf()` directly** with `"true"` and `"false"`.  
   - Alternatively, we can use **`const char*`** variables for better readability.

---

### **Corrected Code:**
```c
#include <stdio.h>

int main() {
    int a, b;

    // Input two integers
    printf("Enter two integers (a and b): ");
    scanf("%d %d", &a, &b);

    // Logical operations
    printf("\nLogical Operations Results:\n");

    // Using ternary operator to print true/false
    printf("(a > 0) && (b > 0): %s\n", (a > 0 && b > 0) ? "true" : "false");
    printf("(a > 0) || (b > 0): %s\n", (a > 0 || b > 0) ? "true" : "false");
    printf("!(a > 0): %s\n", (!(a > 0)) ? "true" : "false");

    return 0;
}
```

---

### **Alternative Using `const char*`:**
```c
#include <stdio.h>

int main() {
    int a, b;
    
    // Input two integers
    printf("Enter two integers (a and b): ");
    scanf("%d %d", &a, &b);

    // Define true/false strings
    const char *trueStr = "true";
    const char *falseStr = "false";

    // Logical operations
    printf("\nLogical Operations Results:\n");
    printf("(a > 0) && (b > 0): %s\n", (a > 0 && b > 0) ? trueStr : falseStr);
    printf("(a > 0) || (b > 0): %s\n", (a > 0 || b > 0) ? trueStr : falseStr);
    printf("!(a > 0): %s\n", (!(a > 0)) ? trueStr : falseStr);

    return 0;
}
```

---

### **Expected Output (Example Runs):**
#### **Case 1: a = 5, b = 3**
```
Enter two integers (a and b): 5 3

Logical Operations Results:
(a > 0) && (b > 0): true
(a > 0) || (b > 0): true
!(a > 0): false
```

#### **Case 2: a = -2, b = 0**
```
Enter two integers (a and b): -2 0

Logical Operations Results:
(a > 0) && (b > 0): false
(a > 0) || (b > 0): false
!(a > 0): true
```

---

### **Explanation:**
1. **Logical AND (`&&`)** → `true` only if **both** conditions are `true`.
2. **Logical OR (`||`)** → `true` if **at least one** condition is `true`.
3. **Logical NOT (`!`)** → **Reverses** the condition.

Your code contains **syntax errors**, mainly in arithmetic operations and missing operators. Below is the **corrected and complete version**:

---

### **Key Fixes:**
1. **Fixed Arithmetic Operators:**
   - `difference = num1 num2;` → should be `difference = num1 - num2;`
   - `product num1 num2;` → should be `product = num1 * num2;`
   - `remainder = num1% num2;` → should be `remainder = num1 % num2;`

2. **Ensured Proper `printf()` Formatting:**
   - `printf("%d %d = %d\n", num1, num2, difference);` → Fixed to include `-`
   - `printf("%d %d = %d\n", num1, num2, product);` → Fixed to include `*`
   - `printf("%d / %d = %.2f\n", num1, num2, quotient);` → Ensured floating-point output.
   - `printf("%d %% %d = %d\n", num1, num2, remainder);` → Used `%%` to print `%`.

---

### **Corrected Code:**
```c
#include <stdio.h>

int main() {
    int num1, num2;
    int sum, difference, product, remainder;
    float quotient;

    // Input two integers
    printf("Enter two integers: ");
    scanf("%d %d", &num1, &num2);

    // Perform arithmetic operations
    sum = num1 + num2;
    difference = num1 - num2;
    product = num1 * num2;
    quotient = (float) num1 / num2; // Typecasting for accurate division
    remainder = num1 % num2;

    // Output results
    printf("\nResults:\n");
    printf("%d + %d = %d\n", num1, num2, sum);
    printf("%d - %d = %d\n", num1, num2, difference);
    printf("%d * %d = %d\n", num1, num2, product);
    printf("%d / %d = %.2f\n", num1, num2, quotient);
    printf("%d %% %d = %d\n", num1, num2, remainder);

    return 0;
}
```
**function in c**:  
---

### **Expected Output (Example Run):**
```
Enter two integers: 10 3

Results:
10 + 3 = 13
10 - 3 = 7
10 * 3 = 30
10 / 3 = 3.33
10 % 3 = 1
```

### **array:**
```
include<stdio.h>

#include<conio.h>

main()

{

int a[4]://declaration of single dimensional array of size 4

int i,j;

clrscr();

printf ("Enter the value in array");

for(i=0;i<4;i++)

{

scanf (d",&a[i]);

}

// it is helping us inserting the value in array a

printf ("Outout for(j=0; j<4; j++)

{

printf("%d",a[j]);

}

// it is helping us reteriving the value in array a

getch();

}
```

### Corrected Code:
```c
#include <stdio.h>

void printString(char arr[]);

int main() {
    char firstname[] = "saujanya";
    
    printString(firstname); // Call the function to print the string
    
    return 0;
}

void printString(char arr[]) {
    for (int i = 0; arr[i] != '\0'; i++) { // Check for the null terminator
        printf("%c", arr[i]);
    }
    printf("\n"); // Optional: Add a newline for better formatting
}
```

#
### Output:
```
saujanya
``` 

Now your code will correctly print the string `"saujanya"`.# String

```
#include <stdio.h>

void printString(char arr[]);

int main() {
    char name[50];
    scanf("%49s", name); // Limit input size
    printf("Your name is %s\n", name);
    printString(name); // Call the function
    return 0;
}

void printString(char arr[]) {
    for (int i = 0; arr[i] != '\0'; i++) {
        printf("%c", arr[i]);
    }
    printf("\n"); // Print newline for better output formatting
}

```
Let's analyze the expected output of the corrected code.

### **Input:**
```
Alice
```

### **Output:**
```
Your name is Alice
Alice
```

### **Explanation:**
1. The program reads the input `"Alice"`.
2. It prints `"Your name is Alice"`.
3. The `printString(name)` function is called, which prints each character of `"Alice"` sequentially.
4. A newline (`\n`) is added at the end for better formatting.

Would you like me to run this code for verification?

Here’s an example of how the corrected program would behave when executed:

### **Input (User enters in stdin)**
```
Hello, World!
```

### **Output**
```
Hello, World!

Hello, World!
```
---
### **Explanation**
1. `fgets(str, 100, stdin);` reads `"Hello, World!\n"` (including the newline `\n`).
2. `puts(str);` prints it, adding an extra newline.
3. `printString(str);` prints the string character by character, keeping the newline.

If you don't want the extra newline from `puts`, you can modify `fgets` to remove it:

#### **Updated Code (Remove Newline from `fgets`)**
```c
#include <stdio.h>

void printString(char arr[]) {
    for (int i = 0; arr[i] != '\0'; i++) {
        printf("%c", arr[i]);
    }
    printf("\n");
}

int main() {
    char str[100];
    fgets(str, 100, stdin);

    // Remove newline if present
    int i = 0;
    while (str[i] != '\0') {
        if (str[i] == '\n') {
            str[i] = '\0';  // Replace newline with null character
            break;
        }
        i++;
    }

    puts(str);
    printString(str);

    return 0;
}
```

### **Output for Same Input**
```
Hello, World!
Hello, World!
```

Now, there’s no extra newline between outputs. Let me know if you need further changes!



Here’s how the corrected program runs with an example input and output:  

### **Fixed Code:**  
```c
#include <stdio.h>

void printString(char arr[]); 
int countLength(char arr[]);

int main() {
    char name[100];
    
    printf("Enter a string: ");
    fgets(name, 100, stdin);

    printf("Length is: %d\n", countLength(name));
    printf("You entered: ");
    printString(name);

    return 0;
}

int countLength(char arr[]) {
    int count = 0;
    while (arr[count] != '\0') {
        count++;
    }

    // Remove trailing newline character (if present)
    if (count > 0 && arr[count - 1] == '\n') {
        return count - 1;
    }

    return count;
}

void printString(char arr[]) {
    for (int i = 0; arr[i] != '\0'; i++) {
        printf("%c", arr[i]);
    }
}
```

---

### **Example Execution:**  
#### **Input:**  
```
Enter a string: Hello World
```

#### **Output:**  
```
Length is: 11
You entered: Hello World
```

---

### **Explanation:**
1. **User enters** `"Hello World"` (11 characters + `\n` from `fgets`).
2. **`countLength` function:**  
   - Counts the characters in the array.
   - Detects the newline character (`\n`) and excludes it.
   - Returns `11` instead of `12` (correct length).
3. **`printString` function:**  
   - Prints the string properly without adding an extra newline.  

Let me know if you need modifications!
