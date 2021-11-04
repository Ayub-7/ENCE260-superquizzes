#include <stdio.h>


// A function to read a small format (8-bit) number
int readInput(unsigned char input[], size_t inputMaxLength);
int readUCharInt(unsigned char* input);
int splitInput(unsigned char input[], size_t inputLength, int section, unsigned char part[], size_t maxPartLength);



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

int splitInput(unsigned char input[], size_t inputLength, int section, unsigned char part[], size_t maxPartLength)
{
    int i = 0;
    int num = 457792;
    int count = 0;
    int sec = 0;
    if (section == 0) {
        while (num != input[0]) {
            if (i >= maxPartLength) {
                return -1;
            }
            if (input[i+1] == input[0]) {
                return count;
            }
            part[i] = input[i+1];
            num = input[i+1];
            i++;
            count++;
        }
    } else {
        while (num != input[0]) {
            if (i >= maxPartLength) {
                return -1;
            }
            num = input[i+1];
            i++;
        }
        i += 1;
        while (i < inputLength) {
            if (i >= maxPartLength) {
                return -1;
            }
            part[sec] = input[i];
            i++;
            sec++;
            count++;
        }

    }
    return count;


}