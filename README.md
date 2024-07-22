Simple number guessing game with C++


		
		#include <stdio.h>
		#include <stdlib.h>
		#include <time.h>
		#include <conio.h>
		#include <math.h>




	int main(int argc, char *argv[]) {
			int sayilar[6], tahmin[6],dogrusayisi= 0;
			srand(time(0));
			char tus, button,c,g,f,d,t,z,p,v,i;
			d=187,c=205,p=200,v=188,f=186,g=201;
	do{
		
		srand((unsigned) time(NULL));
		for(i=0;i<6;i++)
		{
			tahmin[i]=rand() %50 + 1;
		}
		system("color 2f");
		system("cls");	
		printf("\n\n\n\n\n\t\t\t\t%c",g);	    
		for(t=0;t<49;t++){	
		printf("%c",c);
		}
		printf("%c",d);
		printf("\n\t\t\t\t%c\t\t\t\t\t\t\  %c",f,f);
		printf("\n\t\t\t\t%c\t\t\t\t\t\t\  %c",f,f);
		printf("\n\t\t\t\t%c\t\t SAYI TAHMINI OYUNU   \t\t  %c",f,f);
		printf("\n\t\t\t\t%c\t\t   HOSGELDINIZ  \t\t  %c",f,f);
		printf("\n\t\t\t\t%c\t\t\t\t\t\t\  %c",f,f);
		printf("\n\t\t\t\t%c\t    6 adet sayi tahmin ediniz  \t\t  %c",f,f);
		printf("\n\t\t\t\t%c      Devamm etmek icin D veya d tusuna basiniz  %c",f,f);
		printf("\n\t\t\t\t%c\t  CIKIS icin ESC tusuna basiniz",f);
		printf("\t\t  %c",f);
		printf("\n\t\t\t\t%c\t\t\t\t\t\t\  %c",f,f);
		printf("\n\t\t\t\t%c\t\t\t\t\t\t\  %c",f,f);
		printf("\n\t\t\t\t%c\t\t\t\t\t\t\  %c",f,f);
		printf("\n\t\t\t\t%c\t\t\t\t\t\t\  %c",f,f);
		printf("\n\t\t\t\t%c\t\t\t\t\t\t\  %c",f,f);
		printf("\n\t\t\t\t%c",p);
		
		for(t=0;t<49;t++){	
		printf("%c",c);
		}
		printf("%c",v);

	
		tus=getch();
		if(tus==27){
			printf("\n\n\n\nCikmak istediginizden eminmisiniz? (E/H) ");
			tus=getch();
			if(tus == 'e'||tus=='E')
			{
				return 0;
			}
			else
			{
				system("cls");
			}
		}
		if(tus=='d' || tus=='D'){
		system("cls");
		system("color 5F");
			
		for( i=0;i<6;i++){
		system("cls");
		system("color 5F");
	    printf("\n\n\n\n\n\t\t\t\t%c",g);
		for(t=0;t<49;t++){	
		printf("%c",c);
		}
		printf("%c",d);
		printf("\n\t\t\t\t%c\t\t\t\t\t\t\  %c",f,f);
		printf("\n\t\t\t\t%c\t\t\t\t\t\t\  %c",f,f);
		printf("\n\t\t\t\t%c\t\t SAYI TAHMINI OYUNU   \t\t  %c",f,f);
		printf("\n\t\t\t\t%c\t\t\t\t\t\t\  %c",f,f);
		printf("\n\t\t\t\t%c\t\t\t\t\t\t\  %c",f,f);
		printf("\n\t\t\t\t%c",p);
		for(t=0;t<49;t++){	
		printf("%c",c);
		}
		printf("%c",v);
		
			printf("\n\n\n\t\t\t\t\t%d. sayisini giriniz: ",i+1);
			scanf("%d",&sayilar[i]);
		}
		for( i = 0 ; i < 6 ;i++)
		{
			if(tahmin[i] == sayilar[i])
			{
				dogrusayisi++;
			}
		}
			printf("\n\n\n\t\t\t\t\tGirilen sayilar   : ");
		for( i = 0 ; i < 6 ;i++)
		{
			printf("%d  ",sayilar[i]);
		}
		printf("\n\t\t\t\t\tUretilen sayilar  : ");
		for( i = 0 ; i < 6 ;i++)
		{
			printf("%d  ",tahmin[i]);
		}
		printf("\n\t\t\t\t\tTahmin sayisi %d",dogrusayisi);
		if(dogrusayisi == 0)
		{
			printf("\n\t\t\t\t\tMalesef hicbir sayi bileediniz .Skorunuz : 0");
		}
		else if(dogrusayisi == 6){
			printf("\n\t\t\t\t\tBINGO! Tebrikler Tum sayilari bildiniz.  skorunuz : %d",(int)pow(10,dogrusayisi));
		}
		else
		{
			printf("\n\t\t\t\t\tTebrikler!%d sayi bildiniz. Skorunuz : %d",dogrusayisi,(int)pow(10,dogrusayisi));	
		}
		printf("\n\t\t\t\t\tyeniden denemek icin bir tusa basiniz");
		
		tus=getch();
	
		if(tus == 27)
		{
			printf("\nCikmak istediginizden eminmisiniz? (E/H)");
			tus = getch();
			if(tus=='e' || tus=='E'){
				return 0;
			}else{
				system("cls");
			}
		}

	}
		}while(tus!='h' || tus!='H');

}
