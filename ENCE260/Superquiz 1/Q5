#include <stdio.h>


// A function to read a small format (8-bit) number
int readInput(unsigned char input[], size_t inputMaxLength);
int readUCharInt(unsigned char* input);
int splitInput(unsigned char input[], size_t inputLength, int section, unsigned char part[], size_t maxPartLength);
void decryptMessage(unsigned char key[], size_t keyLength, unsigned char message[], size_t messageLengtha);




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

void decryptMessage(unsigned char key[], size_t keyLength, unsigned char message[], size_t messageLength)
{
    int a_1 = 0;
    int b_1 = 0;
    if (keyLength > 1) {

        for (int i = 0; i < messageLength; i++) {
            if (i >= keyLength) {
                while (a_1+i < messageLength) {
                    if (b_1 >= keyLength) {
                        b_1 = 0;
                        message[a_1+i] = message[a_1+i] - key[b_1];
                        a_1++;
                        b_1++;
                    }
                    message[a_1+i] = message[a_1+i] - key[b_1];
                    a_1++;
                    b_1++;
                }
                break;
            }
            message[i] = message[i] - key[i];
        }
    } else {
        for (int i = 0; i < messageLength; i++) {
            message[i] = message[i] - key[0];
        }
    }
}

int main()
{
#define MAX_INPUT_MESSAGE_LENGTH 4096
#define MAX_KEY_LENGTH 1024
#define MAX_TEXT_LENGTH 3072
    unsigned char input[MAX_INPUT_MESSAGE_LENGTH];
    int inputLength = readInput(input, MAX_INPUT_MESSAGE_LENGTH);

    unsigned char part[MAX_TEXT_LENGTH];
    unsigned char part1[MAX_TEXT_LENGTH];

    int partLength;
    int keyLength;
    partLength = splitInput(input, inputLength, 1, part, MAX_TEXT_LENGTH);
    keyLength = splitInput(input, inputLength, 0, part1, MAX_TEXT_LENGTH);
    decryptMessage(part1, keyLength, part, partLength);

    for(int i=0; i < partLength; i++) {
        printf("%c", part[i]);
    }

}
