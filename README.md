#include <stdio.h>

int main() {
    int input[] = {1, 2, 8, 9, 12, 46, 76, 82, 15, 20, 30};
    int count[10] = {0}; // Initialize an array to store the count of multiples (0 to 9)

    // Calculate the count of multiples for each number
    for (int i = 0; i < sizeof(input) / sizeof(input[0]); i++) {
        for (int j = 1; j <= 9; j++) {
            if (input[i] % j == 0) {
                count[j]++;
            }
        }
    }

    // Print the results
    printf("Output:\n");
    for (int i = 1; i <= 9; i++) {
        printf("%d: %d\n", i, count[i]);
    }

    return 0;
}
