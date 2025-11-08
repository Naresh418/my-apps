// simple_pin.c
#include <stdio.h>

int main(void) {
    const int CORRECT_PIN = 1234;  // set the "stored" PIN here
    int pin;
    int attempts = 3;

    printf("Enter your 4-digit PIN. You have %d attempts.\n", attempts);

    while (attempts > 0) {
        printf("PIN: ");
        if (scanf("%d", &pin) != 1) {
            // clear invalid input
            int c; while ((c = getchar()) != '\n' && c != EOF) {}
            printf("Invalid input. Try again.\n");
            continue;
        }

        if (pin == CORRECT_PIN) {
            printf("PIN accepted. Access granted.\n");
            return 0;
        } else {
            attempts--;
            if (attempts > 0)
                printf("Wrong PIN. %d attempt(s) remaining.\n", attempts);
            else
                printf("Wrong PIN. No attempts remaining. Card blocked.\n");
        }
    }

    return 0;
}
