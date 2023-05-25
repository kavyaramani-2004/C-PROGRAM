#include <stdio.h>
#include <ctype.h>
int main() {
    char str[100];
    int uppercaseCount = 0, lowercaseCount = 0, i = 0;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);
    while (str[i] != '\0') {
        if (isupper(str[i]))
            uppercaseCount++;
        else if (islower(str[i]))
            lowercaseCount++;
        i++;
    }
    printf("Number of uppercase letters: %d\n", uppercaseCount);
    printf("Number of lowercase letters: %d\n", lowercaseCount);
    return 0;
}
