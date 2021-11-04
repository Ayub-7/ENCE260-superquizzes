//returns text cipher
size_t readMessage(FILE* file, char text[], size_t maxTextSize)
{
    int textLen = 0;
    textLen = readText(file, text, maxTextSize);

    int i_n = 0;
    while (i_n < strlen(text)) {
        if (text[i_n] >= 32 && text[i_n] <= 126) {
            text[i_n] -= 31;
            i_n++;
        } else if (text[i_n] == '\t') {
            text[i_n] = 96;
            i_n++;
        } else if (text[i_n] == '\n') {
            text[i_n] = 97;
            i_n++;
        }
    }

    text[i_n] = '\0';

    return textLen;
}