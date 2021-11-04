#include <stdio.h>


// A function to read a small format (8-bit) number
int readInput(unsigned char input[], size_t inputMaxLength);
int readUCharInt(unsigned char* input);


int readUCharInt(unsigned char* input)
{
    int size;
    size = scanf("%hhu", input);
    return size;
}


int readInput(unsigned char input[], size_t inputMaxLength)
{
    int value = 0;
    int i = 0;
    unsigned char c = 0;

    while ((readUCharInt(&c)) != -1 && value < inputMaxLength) {
        input[i] = c;
        if (value > inputMaxLength) {
            return -1;
        }
        value++;
        i++;
    }
    if (value >= inputMaxLength) {
        return -1;
    }
    return value;
}

