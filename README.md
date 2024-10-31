#include <stdio.h>
int main() {
    int amount;
    int denominations[] = {2000, 500, 200, 100, 50, 20, 10, 5, 2, 1};
    int counts[10];
    printf("Enter Amount: ");
    scanf("%d", &amount); 
    for (int i = 0; i < 10; i++) {
        if (amount >= denominations[i]) {
            counts[i] = amount / denominations[i];
            amount = amount % denominations[i];
            printf("The Currency of Rs %d are: %d\n", denominations[i], counts[i]);
        }
    }
} 
