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
