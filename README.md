# Project-3
Random password generator 
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int length, i;
    
    // Characters allowed in the password
    char characters[] = "abcdefghijklmnopqrstuvwxyz"
                        "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
                        "0123456789"
                        "!@#$%^&*()_+[]{}?|<>";

    printf("Enter password length: ");
    scanf("%d", &length);

    srand(time(0)); // Seed for randomness

    printf("Generated Password: ");
    for (i = 0; i < length; i++) {
        int index = rand() % (sizeof(characters) - 1);
        printf("%c", characters[index]);
    }

    printf("\n");
    return 0;
}
