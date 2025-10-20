# Triangle Text Art

## 1. Draw a Rightangled Triangle 
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
