# BIBAPP-development
development of a simple app for school exam
//inputs
#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>
#include <string.h>
#include <locale.h>

//colors
#define RED "\e[0;31m"
#define GREEN "\e[0;32m"
#define YELLOW "\e[0;33m"
#define BLUE "\e[0;34m"
#define CYAN "\e[0;36m"
#define MAGENTA "\e[0;35m"
#define RESET "\e[0m"

//backgrounds
#define BLKB "\e[40m"
#define REDB "\e[41m"
#define GRNB "\e[42m"
#define YELB "\e[43m"
#define BLUB "\e[44m"
#define MAGB "\e[45m"
#define CYNB "\e[46m"
#define WHTB "\e[47m"

//global variants 
int i,n,m,j;

//program structs
struct bib{
	int na;
	char nome[30];
	float ava;
	char dec[500];
	char sava[5];
	char com[200];
	char des[30];
};

struct bib app;
FILE *fx;

//file creation

//file management

//program functions 2º layer
void a1_(){
	system("CLS");
	printf(RED"[PAGE 1.]\n---------\n");
	printf(YELLOW"\n @@@@@@   @@@@@@@   @@@@@@@    @@@@@@   \n@@@@@@@@  @@@@@@@@  @@@@@@@@  @@@@@@@   \n@@!  @@@  @@!  @@@  @@!  @@@  !@@       \n!@!  @!@  !@!  @!@  !@!  @!@  !@!       \n@!@!@!@!  @!@@!@!   @!@@!@!   !!@@!!    \n!!!@!!!!  !!@!!!    !!@!!!     !!@!!!   \n!!:  !!!  !!:       !!:            !:!  \n:!:  !:!  :!:       :!:           !:!   \n::   :::   ::        ::       :::: ::   \n :   : :   :         :        :: : :    ");
	printf(RED"\n\nNow you can scroll in this page and search for your apps manually. You can also use [ENTER] to skip to the next page!                               »[ENTER TO CONTINUE]«\n\n\n"RESET);
	fx = fopen("bibapp.txt","r");
	while(fscanf(fx,"%s %s %f %s",app.nome,app.des,&app.ava,app.dec)!=EOF){
			printf(RED"--------------------\n|\n|%s\n|\n--------------------\nDeveloper: "RESET"%s\n\n"RED"- Rating: "RESET"%.1f\n"RED"Description: ",app.nome,app.des,app.ava,app.dec); //can't print the information from the file!!!
		}
	fclose(fx);
	getch();
	
	
}

void a2_(){
	
}

void a3_(){
	
}

//program functions
void cont(){
	system("CLS");
	printf(YELLOW"How many apps do you want to create?\nA.: "RESET);
	scanf("%d",&n);
	for(i=1;i<=n;i++){
		printf(RED"\n\nApp %d Data: "RESET);
		printf(RED"\n\nName: "RESET);
		fflush(stdin);
		gets(app.nome);
		printf(RED"\nDeveloper: "RESET);
		fflush(stdin);
		gets(app.des);
		printf(RED"\nDescription: "RESET);
		fflush(stdin);
		gets(app.dec);
		getch();
		system("CLS");
	}
}

void viz(){
	char opc_;
	do{
		system("CLS");
		printf(YELLOW"\n @@@@@@   @@@@@@@   @@@@@@@    @@@@@@   \n@@@@@@@@  @@@@@@@@  @@@@@@@@  @@@@@@@   \n@@!  @@@  @@!  @@@  @@!  @@@  !@@       \n!@!  @!@  !@!  @!@  !@!  @!@  !@!       \n@!@!@!@!  @!@@!@!   @!@@!@!   !!@@!!    \n!!!@!!!!  !!@!!!    !!@!!!     !!@!!!   \n!!:  !!!  !!:       !!:            !:!  \n:!:  !:!  :!:       :!:           !:!   \n::   :::   ::        ::       :::: ::   \n :   : :   :         :        :: : :    ");
		printf("\n\nHere you can see or search for your favourite apps."RESET"\n\n----------------------------------------------\n|1. - If you want to see the apps, press '1'.|\n|2. - If you want to search apps, press '2'. |\n|3. - If you want to rate apps, press '3'.   |\n----------------------------------------------\n\nPress '0' to return.\n"YELLOW"\nChoose your option: "RESET);
		printf(YELLOW"\n\n\n@@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@\n@@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@\n@@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  \n@@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!    \n!@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!\n!!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  \n!!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!: \n:!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  \n::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   \n :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    : "RESET);
		opc_=getch();
		switch(opc_){
			case '1': a1_();break;
			case '2': a2_();break;
			case '3': a3_();break;
		}
	}while(opc_ != '0');
}

//main
int main(){
	setlocale(LC_ALL, "Portuguese");
	char opc;
	do{
		system("CLS");
		printf(YELLOW"\n\n@@@@@@@   @@@  @@@@@@@    @@@@@@   @@@@@@@   @@@@@@@   \n@@@@@@@@  @@@  @@@@@@@@  @@@@@@@@  @@@@@@@@  @@@@@@@@  \n@@!  @@@  @@!  @@!  @@@  @@!  @@@  @@!  @@@  @@!  @@@  \n!@   @!@  !@!  !@   @!@  !@!  @!@  !@!  @!@  !@!  @!@  \n@!@!@!@   !!@  @!@!@!@   @!@!@!@!  @!@@!@!   @!@@!@!   \n!!!@!!!!  !!!  !!!@!!!!  !!!@!!!!  !!@!!!    !!@!!!    \n!!:  !!!  !!:  !!:  !!!  !!:  !!!  !!:       !!:       \n:!:  !:!  :!:  :!:  !:!  :!:  !:!  :!:       :!:       \n :: ::::   ::   :: ::::  ::   :::   ::        ::       \n:: : ::   :    :: : ::    :   : :   :         :        \n\nHere you'll find some of your favourite apps. You can also see their respective developer, rating and description and even create your own app!\nSearch, develop and renew. Thank you for choosing BIBAPP!"RESET);
		printf(YELLOW"\n\n:::::::::::::  :::::::::::::  :::::::::::::  :::::::::::::  :::::::::::::  :::::::::::::  :::::::::::::  :::::::::::::"RESET"\n\nProcede inserting '1' or create your own app inserting '2': "YELLOW"\n\n@@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@\n@@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@\n@@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  @@@  \n@@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!  @@!    \n!@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!  !@!\n!!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  !!!  \n!!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!:  !!: \n:!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  :!:  \n::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   ::   \n :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    :    : ");
		opc=getch();
		switch(opc){
			case '1': viz();break;
			case '2': cont();break;
			}
	}while(opc!='0');
}
