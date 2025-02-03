#include <stdio.h>
int main()
{
  int amount=100000;
  printf("Enter choice 1:account balance \nEnter choice 2:withdraw \nEnter choice 3:deposit\n");
  int a;
  while(1){
     scanf("%d",&a);
    if(a==1){
      printf("Available balance:%d\n",amount);
    }
    else if(a==2){
      printf("Enter amount to be withdraw:");
      int rs;
      scanf("%d",&rs);
      if(rs>amount){
      printf("Insuffiscient funds\n");
      }
      else{
        amount=amount-rs;
        printf("Account balance:%d\n",amount);
      }
    }
    else if(a==3){
      int drs;
      amount=amount+drs;
      printf("Enter amount to be deposit:");
      scanf("%d",&drs);
      printf("Account balance:%d\n",amount);
    }
    else{
      printf("Enter valid number (1 to 3)");
    }
    printf("If you want to continue press(y):");
    char a;
    scanf(" %c",&a);
    if(a!='y'){
        break;
    }
  }
  return 0;
}
