# Triangle Text Art

## 1. Draw a Right-angled Triangle 
Draw a triangle of a given size.

E.g., if the input size is 4, the triangle will look like this-
```
*
* *
* * *
* * * *
```

Here is a solution to it in `C`-
```C
#include <stdio.h>

int main(){
    printf("Enter a size: ");
    int size;
    scanf("%d", &size);
    int i;
    int j;
    for (i = 1; i <= size; i++){
        for (j = 1; j <= i; j++){
            printf("* ");
        }
        printf("\n");
    }
    return 0;
}
```

## 2. Update to an Equilateral Triangle
So, now the triangle will look like-
```
   *
  * *
 * * *
* * * *
```

Solution-
```C
#include <stdio.h>

int main(){
    printf("Enter a number: ");
    int num;
    scanf("%d", &num);
    int i;
    int j;
    int k;
    for (i = num; i >= 0; i--){
        for (j = 1; j <= i; j++){
            printf(" ");
        }
        for (k = j; k <= num; k++){
            printf("* ");
        }
        printf("\n");
    }
    return 0;
}
```

## 3. Improve the Drawing
Instead of space, use `*`

```
   *
  ***
 *****
*******
```

Solution-
```C
#include <stdio.h>

int main(){
    printf("Enter a size: ");
    int size;
    scanf("%d", &size);
    int i;
    int j;
    int k;
    for (i = 1; i <= size; i++){
        for (k = 1; k <= size - i; k++){
            printf(" ");
        }
        for (j = 1; j < 2 * i ; j++){
            printf("*");
        }
        printf("\n");
    }
    return 0;
}
```

## 4. Now, Reverse it
So, it looks like-
```
*******
 *****
  ***
   *
```

Solution-
```C
#include <stdio.h>

int main(){
    printf("Enter a size: ");
    int size;
    scanf("%d", &size);
    int i;
    int j;
    int k;
    for (i = 0; i < size; i++){
        for (k = 1; k <= i; k++){
            printf(" ");
        }
        for (j = 1; j < 2*(size - i); j++){
            printf("*");
        }
        printf("\n");
    }
    return 0;
}
```

## 5. Draw a Diamond 
Modiifying the same code, draw a diamond of a given size.

E.g, a diamond of size 4 will look like-
```
 *
***
***
 *
```
And a diamond of size 5 will look like-
```
  *
 ***
*****
 ***
  *
```

**Hint**: A diamond shape is actually a stacked regular triangle and a reverse triangle 

Solution-
```C
#include <stdio.h>

int main(){
    printf("Enter a size: ");
    int size;
    scanf("%d", &size);
    int i;
    int j;
    int k;
    int x;
    int y;
    int z;
    int m;
    if (size % 2 == 0){
        for (i = 1; i <= size / 2; i++){
            for (j = 1; j <= (size / 2) - i; j++){
                printf(" ");
            }
            for (k = 1; k < 2*i; k++){
                printf("*");
            }
            printf("\n");
        }
        for (x = 0; x < size / 2; x++){
            for (y = 1; y <= x; y++){
                printf(" ");
            }
            for (z = 1; z < 2 * ((size / 2) - x); z++){
                printf("*");
            }
            printf("\n");
        }
    }
    else {
        for (i = 1; i <= size / 2; i++){
            for (j = 0; j <= (size / 2) - i; j++){
                printf(" ");
            }
            for (k = 1; k < 2*i; k++){
                printf("*");
            }
            printf("\n");
            }
        for (m = 1; m <= size; m++){
            printf("*");
        }
        printf("\n");

        for (x = 0; x < size / 2; x++){
            for (y = 0; y <= x; y++){
                printf(" ");
            }
            for (z = 1; z < 2 * ((size / 2) - x); z++){
                printf("*");
            }
            printf("\n");
            }
        }

    return 0;
}
```
## 6. Now, Draw a Boundary Around The Diamond
It should be like-
```
***********
*         *
*    *    *
*   ***   *
*  *****  *
*  *****  *
*   ***   *
*    *    *
*         *
***********
```

Solution-
```C
#include <stdio.h>

int main(){
    printf("Enter a size: ");
    int size;
    scanf("%d", &size);
    int i;
    int j;
    int k;
    int x;
    int y;
    int z;
    int m;
    int a;
    int b;
    int c;
    int d;
    int p;
    int q;
    if (size % 2 == 0){
        for (a = 1; a <= size + 3; a++){
            printf("*");
        }
        printf("\n");
        printf("*");
        for (c = 1; c <= size + 1; c++){
            printf(" ");
        }
        printf("*");
        printf("\n");
        for (i = 1; i <= size / 2; i++){
            printf("* ");
            for (j = 1; j <= (size / 2) - i; j++){
                printf(" ");
            }
            for (k = 1; k < 2*i; k++){
                printf("*");
            }
            for (p = 1; p <= (size / 2) - i; p++){
                printf(" ");
            }
            printf(" *");
            printf("\n");
        }
        for (x = 0; x < size / 2; x++){
            printf("* ");
            for (y = 1; y <= x; y++){
                printf(" ");
            }
            for (z = 1; z < 2 * ((size / 2) - x); z++){
                printf("*");
            }
            for (p = 1; p <= x; p++){
                printf(" ");
            }
            printf(" *");
            printf("\n");
        }
        printf("*");
        for (d = 1; d <= size + 1; d++){
            printf(" ");
        }
        printf("*");
        printf("\n");
        for (b = 1; b <= size + 3; b++){
            printf("*");
        }
    }
    else {
        for (a = 1; a <= size + 4; a++){
            printf("*");
        }
        printf("\n");
        printf("*");
        for (c = 1; c <= size + 2; c++){
            printf(" ");
        }
        printf("*");
        printf("\n");
        for (i = 1; i <= size / 2; i++){
            printf("* ");
            for (j = 0; j <= (size / 2) - i; j++){
                printf(" ");
            }
            for (k = 1; k < 2*i; k++){
                printf("*");
            }
            for (p = 0; p <= (size / 2) - i; p++){
                printf(" ");
            }
            printf(" *");
            printf("\n");
            }
        printf("* ");
        for (m = 1; m <= size; m++){
            printf("*");
        }
        printf(" *");
        printf("\n");

        for (x = 0; x < size / 2; x++){
            printf("* ");
            for (y = 0; y <= x; y++){
                printf(" ");
            }
            for (z = 1; z < 2 * ((size / 2) - x); z++){
                printf("*");
            }
            for (p = 0; p <= x; p++){
                printf(" ");
            }
            printf(" *");
            printf("\n");
        }
        printf("*");
        for (d = 1; d <= size + 2; d++){
            printf(" ");
        }
        printf("*");
        printf("\n");
        for (b = 0; b <= size + 3; b++){
            printf("*");
        }
        }

    return 0;
}

