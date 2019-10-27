# data-lab-2

#include<stdio.h>
#define success_value 99999
#define null_value -99999
int list[5];
int length;
void initialize()
{
    length=0;
}
void insertItem(int value)
{
    list[length]=value;
    length=length+1;
    //return success_value;
}
void print()
{
    int i;
    for(i=0;i<length;i++)
    {
        printf("%d ",list[i]);
    }
}
int getItem(int pos)
{
int res;
res=list[pos];
return res;
}
int deleteItemAt(pos)
{
    if(pos>=0 && pos<length)
    {
    list[pos] = list[length-1];
    length = length -1;
    return success_value;
    }
    else
    {
        return null_value;
    }
}
int main()
{
    int c,input,ret,inp;
    initialize();
    scanf("%d",&input);
    insertItem(input);
    scanf("%d",&input);
    insertItem(input);
    scanf("%d",&input);
    insertItem(input);
    scanf("%d",&input);
    insertItem(input);
    scanf("%d",&input);
    insertItem(input);
    //c=getItem(2);
    print();
    scanf("%d",&inp);
    printf("\n");
    //printf("%d",c);
    ret = deleteItemAt(inp);
    if(ret == success_value)
    {
        printf("successfully deleted\n");
    }
        else
        {
            printf("not deleted\n");
        }
        print();
}
