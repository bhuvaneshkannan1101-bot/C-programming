

### 1.Question:

Write a C program to traverse a 2D matrix and print the values until a negative number is found. Use break statement.

### Program:

```c
#include <stdio.h>

int main() {
    int arr[3][3] = {
        {1, 2, 3},
        {4, -5, 6},
        {7, 8, 9}
    };

    for(int i = 0; i < 3; i++) {
        for(int j = 0; j < 3; j++) {
            if(arr[i][j] < 0) {
                break;
            }
            printf("%d ", arr[i][j]);
        }
    }
    return 0;
}
```

### Output:
<img width="1638" height="495" alt="image" src="https://github.com/user-attachments/assets/4a996a9a-0518-439a-8722-cdb1a2946738" />

### 2.Question:

Write a C program to print numbers from 1 to 100 excluding multiples of 3 and numbers containing digit 5 using continue.

### Program:

```c
#include <stdio.h>

int main() {
    for(int i = 1; i <= 100; i++) {

        if(i % 3 == 0)
            continue;

        int temp = i, flag = 0;

        while(temp > 0) {
            if(temp % 10 == 5) {
                flag = 1;
                break;
            }
            temp /= 10;
        }

        if(flag)
            continue;

        printf("%d ", i);
    }
    return 0;
}
```

### Output:
<img width="1906" height="634" alt="image" src="https://github.com/user-attachments/assets/b172ca60-0173-497a-be00-2ea61095a26a" />

### 3.Question:

Write a C program that performs division and handles division by zero using goto.

### Program:

```c
#include <stdio.h>

int main() {
    int a, b;

retry:
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    if(b == 0) {
        printf("Division by zero not allowed!\n");
        goto retry;
    }

    printf("Result = %d", a / b);
    return 0;
}
```

### Output:
<img width="1887" height="457" alt="image" src="https://github.com/user-attachments/assets/df25554d-6369-49a9-ac8c-5bb1795cdc0b" />

### 4.Question:

Write a C program for a number guessing game using loop, break and return.

### Program:

```c
#include <stdio.h>

int main() {
    int guess, target = 7;

    while(1) {
        printf("Enter guess (-1 to exit): ");
        scanf("%d", &guess);

        if(guess == -1)
            return 0;

        if(guess == target) {
            printf("Correct guess!\n");
            break;
        } else {
            printf("Wrong guess\n");
        }
    }
    return 0;
}
```

### Output:
<img width="1656" height="536" alt="image" src="https://github.com/user-attachments/assets/70543853-c3eb-4a95-934e-8f057c04940b" />

### 5. Question:

Write a program to process array {10, -5, 20, 0, 150, 30} using continue, break, return.

### Program:

```c
#include <stdio.h>

int main() {
    int arr[] = {10, -5, 20, 0, 150, 30};

    for(int i = 0; i < 6; i++) {

        if(arr[i] < 0)
            continue;

        if(arr[i] == 0)
            break;

        if(arr[i] > 100)
            return 0;

        printf("%d ", arr[i]);
    }
    return 0;
}
```

### Output:
<img width="1623" height="527" alt="image" src="https://github.com/user-attachments/assets/4cf96781-c3b0-4db2-89ab-5b306c2849e5" />
