#include <iostream>
using namespace std;

    void add(int st[5],int &top){
int item;
if(top==4)
    cout<<"over flow\n";
else {
    cout<<"The number you want to add: ";
    cin>>item;
    top++;
    st[top]=item;
    }
    }
    void del (int st[5], int &top){
    int item;
    if(top==-1)
        cout<<"Under flow\n";
    else{
    item=st[top];
    top--;
    cout<<"The last number in stack deleted \n";
    //////اخر عنصر بالستاك لان بالطباعة يبدي من الصفر (اول رقم)الى اخر رقم
    }
    }
    void pr(int st[5], int &top){
    for(int i=0;i<=top;i++)
        cout<<st[i]<<endl;
     }
    int main(){
    int st[5];
    int x,top=-1;
    cout<<"1- add item\n2- del item\n3- print stack\n4- stop the program.\n";
    do{
        cout<<"Enter your choses: ";
        cin>>x;
        switch(x){
        case 1: add(st,top);break;
        case 2: del(st,top);break;
        case 3: pr(st,top);break;
        default:cout<<"choses a number among 1 to 3 ^_^\n";
        }}while(x!=4);

    return 0;
}
