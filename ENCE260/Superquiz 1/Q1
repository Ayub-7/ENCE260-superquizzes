#include <stdio.h>

// A function to read a small format (8-bit) number
int readUCharInt(unsigned char* input)
{
    int size;
    size = scanf("%hhu", input);
    return size;
}

int main()
{
    unsigned char input = 0;
    int ans = 0;

    ans = readUCharInt(&input);
    if (input >= 32 && input <= 127) {
        printf("Read number %u with ASCII symbol %c\n", input, input);
    } else if (ans == EOF) {
        printf("No input");
    } else {
        printf("Read number %u - non-printable character", input);
    }
}
