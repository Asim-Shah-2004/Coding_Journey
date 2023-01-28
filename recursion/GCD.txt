// done using Euclid's algorithm
#include <stdio.h>
int GCD(int n1,int n2){
    if(n2!=0){
        GCD(n2,n1%n2);
    }else{
        return n1;
    }
}
int main(){
    int n1,n2;
    printf("Enter 1st digit.\n");
    scanf("%d",&n1);
    printf("Enter 2nd digit.\n");
    scanf("%d",&n2);
    if(n2>n1){
        int temp = n2;
        n2 = n1;
        n1 = temp;
    }
    printf("The GCD of digits are :%d\n",GCD(n1,n2));
    return 0;
}

// refer https://www.youtube.com/watch?v=aHuKHVsgz6M for the algorithm
