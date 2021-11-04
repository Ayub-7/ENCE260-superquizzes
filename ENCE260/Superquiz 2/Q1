//reads text from gile and returns lenght of file
size_t readText(FILE* file, char text[], size_t maxTextSize)
{
    int count = 0;
    int c_h;
    while ((c_h = fgetc(file)) != EOF && count+1 < maxTextSize) {
        text[count] = c_h;
        count++;
    }
    return count;


}