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
