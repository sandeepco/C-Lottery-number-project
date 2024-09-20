# include <stdio.h>
#include <stdlib.h>
#include <time.h>
int main() {
    int number,guess,nguessess = 1;
    srand(time(0));
    number = rand() % 100 +1;
    do{
        printf("Guess the number between 1 yo 100 \n");
        scanf("%d",&guess);
        if(guess>number){
            printf("Lower number please! \n");
        }
        else if(guess<number){
            printf("Greater number Please! \n");
        }
        else
        {
            printf ("Your guessed it in %d attempts \n",nguessess);
        }
        nguessess++;
    }
    while(guess!=number);
    return 0;
}
