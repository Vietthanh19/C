#include<stdio.h>
void THN(int n , char nguon, char trunggian, char dich ){
    if(n==1){
        printf("\t%c---->%c\n",nguon,dich);
        return ;
    }else
    THN(n-1,nguon,dich,trunggian);
    THN(1,nguon,trunggian,dich);
    THN(n-1,trunggian,nguon,dich);
    }
int main(){
    char a='A', b='B', c='C';
    int n;
    printf("Nhap n: ");
    scanf("%d",&n);
    THN(n,a,b,c);
}
