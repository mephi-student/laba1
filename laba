#include <stdio.h>
#include <stdlib.h>
#include <math.h>
#include <string.h>
#include <malloc.h>
//#include <clocale>


char* concatenation() //конкатенация
{
    char* first = (char*)malloc(sizeof(char)*512);
    char* second = (char*)malloc(sizeof(char)*512);
    printf("input first string\n");
    scanf ("%s", first);
    printf("input second string\n");
    scanf ("%s", second);
    char* third = (char*)malloc(strlen(first)+strlen(second)+1);
    memcpy(third, first, strlen(first));
    memcpy(third+strlen(first), second, strlen(second)+1);
    printf("%s\n", third);
    free(first);
    free(second);
    free(third);
}


char* selection() //получение подстроки
{
    char* first = (char*)malloc(sizeof(char)*512);
    int g=0;
    int i, j;
    while (g==0){
    printf("input string\n");
    scanf ("%s", first);
    printf("input numbers\n");
    scanf ("%i %i", &i, &j);
    if (i>j){
        int p=j;
        j=i;
        i=p;
    }
    if (((j-i+1)>strlen(first))||(i>strlen(first))||(j>strlen(first))||(strlen(first)==0))
        g=0;
    else g=1;
    if(g==0)
        printf("Error! Not found\n");
    }
    char* third = (char*)malloc(sizeof(char)*(j-i));
    for (int k=i; k<=j; ++k)
        *(third+k-i)=*(first+k);
    printf("%s", third);
    free (first);
    free (third);
}


int search(char* first, char* second){
    int f=0;
    for (int i=0; i<strlen(first); ++i){
        if(*(first+i)==*(second+0)){
            for (int j=1; j<strlen(second); ++j){
                if(*(first+i+j)==*(second+j))
                    f=f+1;
                else{
                    f=0;
                    break;
                }
            }
        }
    }
    return f;
}



void search_sensitive() //поиск чувствительный к регистру
{
    int f;
    char* first = (char*)malloc(sizeof(char)*512);
    char* second = (char*)malloc(sizeof(char)*512);
    int g=0;
    while (g==0){
    printf("input string\n");
    scanf ("%s", first);
    printf("input substring\n");
    scanf ("%s", second);
    if ((strlen(first)<strlen(second))||(strlen(first)==0)||(strlen(second)==0))
        g=0;
    else g=1;
    if(g==0)
        printf("Error! not found");
        }
    f=search(first, second);
    if(f==0)
        printf ("false");
    else
        printf ("true");
    free(first);
    free(second);
}

void search_insensitive() //поиск нечувствительный к регистру
{
    int f;
    char* first = (char*)malloc(sizeof(char)*512);
    char* second = (char*)malloc(sizeof(char)*512);
    int g=0;
    while (g==0){
    printf("input string\n");
    scanf ("%s", first);
    printf("input substring\n");
    scanf ("%s", second);
    first=strlwr(first);
    second=strlwr(second);
    if ((strlen(first)<strlen(second))||(strlen(first)==0)||(strlen(second)==0))
        g=0;
    else g=1;
    if(g==0)
        printf("Error! Not found");}
    f=search(first, second);
    if(f==0)
        printf ("false");
    else
        printf ("true");
    free(first);
    free(second);
}

void test(){
    int k=0;
    char* first = (char*)malloc(sizeof(char)*512);
    printf ("for test concatenation input 1 \nfor test selection input 2 \nfor test search_sensitive input 3 \nfor test search_insensitive input 4 \n");
    scanf ("%i", &k);
    if (k==1){
        printf(" qwertyui and sdfgh result qwertyuisdfgh \n ");
        concatenation();}
    if (k==2){
        printf("qwertyuiopasd and  3  8 result ertyui \n ");
        selection();}
    if (k==3){
         printf("qwertyui and sdfgh result false \n ");
        search_sensitive();}
    if (k==4){
        printf(" qwertyui and sdfgh result false \n ");
        search_insensitive();}

    printf ("for test concatenation input 1 \nfor test selection input 2 \nfor test search_sensitive input 3 \nfor test search_insensitive input 4 \n");
    scanf ("%i", &k);
    if (k==1){
        printf(" qwerTiip and sDfgh result qwerTiipsDfgh \n ");
        concatenation();}
    if (k==2){
        printf(" qwERtyuiopasd and 2  3 result wE \n ");
        selection();}
    if (k==3){
         printf(" qwERtyui and RTyu result true \n ");
        search_sensitive();}
    if (k==4){
        printf(" qwERTyui and RTyu result true \n ");
        search_insensitive();}
}


int main(){
    char* first = (char*)malloc(sizeof(char)*512);
    int k=10;
    while (k!=0){
        printf (" \n for concatenation input 1 \nfor selection input 2 \nfor search_sensitive input 3 \nfor search_insensitive input 4 \nfor test 5 \nfor end 0 \n ");
        scanf ("%i", &k);
        if (k==1)
            concatenation();
        if (k==2)
            selection();
        if (k==3)
            search_sensitive();
        if (k==4)
            search_insensitive();
        if (k==5)
            test();
    }
    return 0;
}
