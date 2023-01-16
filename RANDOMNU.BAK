#include<stdio.h>
#include<time.h>
#include<stdlib.h>
#include<conio.h>
#include<graphics.h>

void black(){
	printf("\033[0;30m");
}

void red () {
	printf("\033[1;31m");
}

void green(){
	printf("\033[0;32m");
}

void yellow() {
	printf("\033[1;33m");
}

void blue(){
	printf("\033[0;34m");
}

void purple(){
	printf("\033[0;35m");
}

void cyan(){
	printf("\033[0;36m");
}

void white(){
	printf("\033[0;37m");
}

int main()
{
    int number, guess, nguess[2]={1,1}, n, gd=DETECT, gm,i;
    initgraph(&gd, &gm, "C:\\TURBOC3\\BGI");
    clrscr();
    setbkcolor(LIGHTGRAY);
    settextstyle(4,HORIZ_DIR,4);

    setcolor(YELLOW);
    for(i=180;i<=480;i=i+10)
    {
       line(180,110,i,110);
       line(180,280,i,280);
       delay(30);
    }

    for(i=110;i<=280;i=i+10)
    {
       line(180,110,180,i);
       line(480,110,480,i);
       delay(30);
    }
    setcolor(RED);
    outtextxy(200,125,"You need to guess");
    outtextxy(220,160,"a random number");
    outtextxy(200,200,"between 1 to 100");
   // printf("\t\tYou need to guess a random number between 1 to 100\n");
    delay(3000);
    cleardevice();
    setbkcolor(BLUE);
    for(n=1;n<=2;n++)
    {
	    srand(time(0));
	    number = rand() % 100 +1;
	   // printf("The number is %d\n", number);
	    yellow();
	    printf("\t\t\tNow playing player%d:\n",n);
	    for(;;nguess[n-1]++)
	    {
		    purple();
		    printf("Guess the Number:\n");
		    scanf("%d", &guess);
		    if(guess==number)
		    {
			    red();
			    printf("\n\t\tYou Guessed it correct in %d attempts\n", nguess[n-1]);
			    break;
		    }
		    if(guess>number)
			    printf("Enter a lower number\n");
		    if(guess<number)
			    printf("Enter a Higher number\n");
	    }
	    delay(1000);
	    printf("\n");
	    getch();
	    cleardevice();
    }
    setbkcolor(GREEN);
    settextstyle(4,HORIZ_DIR,3);
    setcolor(RED);
    outtextxy(180,110,"CONGRATULATIONS!");
    settextstyle(3,HORIZ_DIR,3);
    setcolor(BLUE);
    if(nguess[0]<nguess[1])
	    outtextxy(180,160,"PLAYER 1 WINS!");
    else if(nguess[0]>nguess[1])
	    outtextxy(180,160,"PLAYER 2 WINS!");
    else
	    outtextxy(100,160,"Both the Players have Same Guessing Power!");
    white();
    printf("Made by NAMAN AGRAWAL");
    getch();
    return 0;
}