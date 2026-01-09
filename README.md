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
