# Print Separate Digits

## 1. Print Reverse
Print the reverse of a given number.

E.g., if the input is 123, the output will be 3 2 1.

A solution-
```C
#include <stdio.h>

int main(){
    printf("Enter a number: ");
    int num;
    scanf("%d", &num);
    int reversenum = 0;
    while (num > 0){
        reversenum = num % 10;
        num = num / 10;
        printf("%d ", reversenum);
    }
    return 0;
}
```

## 2. Print The Digits
Print the number with the digits separately.

E.g., if the input is 123, it will print 1 2 3.

Solution-
```C
#include <stdio.h>

int main(){
    printf("Enter a number: ");
    int num;
    scanf("%d", &num);

    int remainder = 0;
    int reversenum = 0;
    while (num > 0){
        remainder = num % 10;
        num = num / 10;

        reversenum = reversenum * 10;
        reversenum = reversenum + remainder;
    }

    while (reversenum > 0){
        printf("%d ", reversenum % 10);
        reversenum = reversenum / 10;
    }

    return 0;
}
```
This is a solution, but not a good one. There are better ways to solve this. That's the next problem.

## 3. Update The Solution

A solution using stack-
```C
#include <stdio.h>

int main(){
    int stack[10];
    int i = 0;

    printf("Enter a number: ");
    int num;
    scanf("%d", &num);

    while (num > 0){
        stack[i] = num % 10;
        num = num / 10;
        i++;
    }

    int j;
    for (j = i - 1; j >= 0; j--){
        printf("%d ", stack[j]);
    }

    return 0;
}
```


