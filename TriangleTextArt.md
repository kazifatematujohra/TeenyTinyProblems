# TeenyTinyProblems

### 1. Draw a triangle 
#### Take a size as input and print a triangle. 
#### For example, if the input is 4, the triangle will look like this -
```
*
* *
* * *
* * * *
```
#### Here is a solution that I wrote
```
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
