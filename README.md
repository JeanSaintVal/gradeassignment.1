#include <stdio.h>
#include <cs50.h>

        int TOTALPOINTSEARNED = 0;
        int TOTALPOINTSPOSSIBLE = 0;

int main(void){
    int assignments = get_int("How many total assignments?:\n");
    for(int i = 0; i < assignments;i++){
        TOTALPOINTSEARNED = TOTALPOINTSEARNED+ get_int ("Total points earned on assignment #%d:\n",i+1);
        TOTALPOINTSPOSSIBLE = TOTALPOINTSPOSSIBLE+ get_int ("Total possible points on assignment #%d:\n",i+1);
       printf("Your current grade is: %d \n",TOTALPOINTSEARNED);
       printf("Total points possible is: %d \n",TOTALPOINTSPOSSIBLE);
    }
    double finalscore = 0;
    finalscore = (double)TOTALPOINTSEARNED/(double)TOTALPOINTSPOSSIBLE*100;
        printf("%f",finalscore);
}
