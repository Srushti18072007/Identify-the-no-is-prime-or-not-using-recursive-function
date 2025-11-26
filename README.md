#include <stdio.h>

int primenum(int num, int i) {  //Fun Definition
    if (i == 1)
        return 1;               

    if (num % i == 0)
        return 0;               

    return primenum(num, i - 1); 
}

int main() {
    int num;                  //Fun Declaration
    printf("Enter a number: ");
    scanf("%d", &num);

    if (primenum(num, num / 2))   //Fun Call
        printf("%d is a prime number\n", num);
    else
        printf("%d is not a prime number\n", num);

    return 0;
}

