//taylor and nina
#include<cs50.h>
#include<ctype.h>
#include<stdlib.h>
#include<math.h>
#include<stdio.h>
#include<string.h>
#include<strings.h>

const int totalquestions = 10;
char answers[totalquestions];
int getscore(char ans, int point, bool tquest);
bool vians(char answer);
int alphanswer(int quest);
int percent(int total);
int score = 0;
bool trueq = true;
char coranswer[10] = {'t','f', 'f', 'f', 't', 'f', 't', 't', 'f', 'f'};
char useranswer[10];
int numswrong[10];

int main(void){
    printf("Please answer with t for True and f for False\n");
    string name = get_string("\nplease enter your name:");
    for(int question = 1; question <= totalquestions; question++){
            if (question == 1){
                trueq = true;
                printf("\n%i. Aragorn's sword is called Anduril Narsil\n", question);}
            else if (question == 2){
                trueq = false;
                printf("\n%i. ct 27-5555's name is echo\n", question);}
            else if (question == 3){
                trueq =false;
                printf("\n%i. Enbo the bouty hunter's uniqe language was the result of poorly read french winnie the pooh books\n", question);}
            else if (question == 4){
                trueq =false;
                printf("\n%i. The sparrow is California's most common bird\n", question);}
            else if (question == 5){
                trueq =true;
                printf("\n%i. Legolas is amazing\n", question);}
            else if (question == 6){
                trueq =false;
                printf("\n%i. Aragorn's horse is named Roheryn\n", question);}
            else if (question == 7){
                trueq =true;
                printf("\n%i. A 5k is more than three miles\n", question);}
            else if (question == 8){
                trueq =true;
                printf("\n%i. Amy Shark used to perform under the name Amy Cushway\n", question);}
            else if (question == 9){
                trueq =false;
                printf("\n%i. Noah Kahan has released Stick Season\n", question);}
            else if (question == 10){
                trueq =false;
                printf("\n%i. The Dewy Decial System is a computer science procedure\n", question);}
        score = alphanswer(question);
    }

    int per = percent(score);
    printf("You were %i%% accurate\n", per);
    if (per>=80){
        printf("\ngood job you know your stuff and by stuff I mean random crap\n");
    }
    else{
        printf("\nwow you need to go read some random facts, or the lord of the rings\n");
    }
    int wrong = 0;
    for(int i = 0; i < totalquestions; i++){
        if (!(useranswer[i] == coranswer[i])){
            numswrong[wrong] = i+1;
            wrong++;
        }
    }
    printf("You got %i questions wrong\n", wrong);
    for(int i=0; i < wrong; i++){
        printf("#%i\n", numswrong[i]);
    }
    FILE *file =fopen("results.txt", "a");
    if (!file){
        return 1;
    }

    //print to file
    fprintf(file,"%s,%i%%\n",name,per);
    //close file
    fclose(file);
}
//prints out possible answers for user to chose
int alphanswer(int quest){
    char answer = get_char("True or False?\n");
    useranswer[quest-1] = answer;
        if(vians(answer) == true){
            return getscore(answer, score, trueq);
        }
    printf("\nplease type one of the letters provided\n");
    return alphanswer(quest);
}
//checks if user gives a viable answer
bool vians(char answer){
    if(answer == 't'){
        return true;}
    else if(answer == 'f'){
        return true;}
    else{
        return false;}
}

//total number of points from user's answers
int getscore(char res, int point, bool tquest){
if (trueq == false){
        if (res == 't'){
            score = score + 0;}
        else if(res == 'f'){
            score = score + 1;}}
if (trueq == true){
        if (res == 't'){
            score = score + 1;}
        else if(res == 'f'){
            score = score + 0;}}
    return score;
}

//calculates user's percentage
int percent(int total){
    total = total*10;
    return total;
}//(:
