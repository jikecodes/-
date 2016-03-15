#include<stdio.h>
#include<stdlib.h>
void LeftShiftOne(char* s,int n){
//保存第一个字符
char t = s[0];
for (int i=1;i<n;i++){
    s[i-1]=s[i];
}
s[n-1]=t;
}
void LeftRtoteString (char* s,int n,int m){
    while(m--){
        LeftShiftOne(s,n);
    }
}

void main(){
    char* s="abcdef";
    LeftRtoteString(s,6,2);
    printf("%s",s);
    system("pause");
}
