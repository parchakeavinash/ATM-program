# ATM-program
#include<iostream>
using namespace std;

class bank{
    char name[20];
    char accounttype[20];
    int accountnumber;
    int balance, deposit, widra;

    public:
    void getvalues(){
        cout<<"Enter the values of \n holder name \n, account type\n, account number\n, and balance:\n ";
        cin>>name>>accounttype>>accountnumber>>balance;
    }

    void depositamount(){
        cout<<"Enter the amount you want to deposit:\n ";
        cin>>deposit;
        balance += deposit;
        cout<<"Your deposit balance is: "<<balance;
    }

    void widramoney(){
        cout<<"\nEnter the amount you want to withdraw: \n";
        cin>>widra;
        if (balance >= widra){
            balance = balance - widra;
            cout<<"After withdrawal, your balance is: \n"<<balance;
        } else {
            cout<<"Insufficient balance.";
        }
    }

    void display(){
        cout<<"\nAccount details are: "<<"\nyour names is: "<<name<<", "<<"\nyour account type is: "<<accounttype<<", "<<"\nyour account number is :"<<accountnumber<<", "<<"\nyour balance is : "<<balance;
    }
};

int main(){
    bank b1;
    b1.getvalues();
    b1.depositamount();
    b1.widramoney();
    b1.display();
    return 0;
}
