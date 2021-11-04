//removes whitespace from the text;
size_t readCipherBook(FILE* file, char text[], size_t maxTextSize)
{

    int textLen = 0;
    textLen = readText(file, text, maxTextSize);

    int i_n = 0;
    int d_n = 0;
    while (i_n < strlen(text)) {
        if (isspace(text[i_n])) {
            textLen -= 1;
            i_n++;
        } else {
            text[d_n] = text[i_n];
            i_n++;
            d_n++;
        }
    }

    text[d_n] = '\0';

    return textLen;
}
