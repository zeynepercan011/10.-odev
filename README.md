# 10.odev

/* bir pozitif tam say� olan n'yi ve n adet karakteri girdi olarak alan bir program. girilen karakterin say� (0-9), alfabetik (a-z/A-Z) ya da �zel karakter
olup olmad���n� belirlemeli(*?�#...) bu belirleme i�lemi bir fonskiyonda yap�lmal�. fonskiyon karakteri parametre olarak almal� ve say� karakteri ise
1,alfabetik karakter ise 2,�zel karakter ise 3 d�nd�rmeli.*/

#include<stdio.h>
int dondur(char);
int main(void)
{
	int n,i,sonuc;
	char kar,enter;
	
	printf("pozitif bir sayi giriniz.");
	scanf("%d" , &n);
	scanf("%c" , &enter);
	
	for(i=1;i<=n;i++)
	{
		printf("karakter giriniz.");
		scanf("%c" , &kar);
		scanf("%c" , &enter);
		
		sonuc=dondur(kar);
		
		switch(sonuc)
		{
			case 1:
				printf("%c sayi karakteridir.\n" , kar);
				break;
			
			case 2:
				printf("%c alfabetik karakterdir.\n" , kar);
				break;
			
			case 3:
				printf("%c ozel karakterdir.\n" , kar);
				break;
			
		}
	}
	return 0;
}

int dondur(char kar)
{
	if('0'<=kar && kar<='9')
	return 1;
	
	else if('A'<=kar && kar<='Z' || 'a'<=kar && kar<='z')
	return 2;
	
	else
	return 3;
}
