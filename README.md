# c-plusplus-Stock-Profit



#include <iostream>
 #include <iomanip>
  using namespace std;
   // function prototype or declaration of function 
    void getInformation(int &, double &, double &, double &, double &);
     void printInformation(int, double, double, double, double);
      double Calculate(int, double, double, double, double);
       int main()
       {
       // declaring variables 
       int NS;      // store the number of shares ;
       double SP;      // store the value of sale price per share 
       double SC;      // store the value of sale commission paid 
      double PP;      // store the value of Purchase price per share 
     double PC;      // store the value of Purchase Commission paid 
    // set format 
   cout<<setprecision(2) << fixed << endl;
  getInformation(NS, SP, SC, PP, PC);
 printInformation(NS, SP, SC, PP, PC);
// return 0 indicates the successful termination 
return 0;
}
 // definition of function getInformation
  void getInformation(int &NS, double &SP, double &SC, double &PP, double &PC)
   {
    cout<<"Please enter the number of shares: " << endl;
     cin >> NS;
      while (NS < 0)
       {
        cout<<"Please enter the number of shares greater than 0: " << endl;
         cin >> NS;
          }
           cout<<"Please enter the Sales price per share:" << endl;
            cin >> SP;
             while (SP < 0)
              {
               cout<<"Please enter the Sales price in positive number: "<< endl;
                cin >> SP;
                }
                cout<<"Please enter the Sale Commission paid: " << endl;
                cin >> SC;
                while(SC < 0)
                {
                cout<<"Please enter the Sale Commission paid in positive number: "<< endl;
               cin >> SC;
              }
             cout<<"Please enter the Purchase Price per share: "<< endl;
            cin >> PP;
           while (PP < 0)
          {
         cout<<"Please enter the Purchase Price per share: "<< endl;
        cin >> PP;
       }
      while (PP < 0)
     {
    cout<<"Please enter the Purchase Price per share in positive number: "<< endl;
   cin >> PP;
  }
 cout<<"Please enter the Purchase Commission: " << endl;
cin >> PC;
while (PC < 0)
{
cout<<"Please enter the purchase commission in positive integer: "<< endl;
 cin >> PC;
  }
   }
    // definition of function Calculate 
     double Calculate(int NS, double SP, double SC, double PP, double PC)
      {
       double Calculate = ((NS * SP) - SC) - ((NS * PP) + PC);
        return Calculate;
         }
          // definition of function printInformation
           void printInformation(int NS, double SP, double SC, double PP, double PC)
            {
            cout<<"so, the answer is  "<<Calculate(NS, SP, SC, PP, PC) << endl;
            if (Calculate(NS, SP, SC, PP, PC) > 0)
            {
            cout<<"The profit is $" <<Calculate(NS, SP, SC, PP, PC) << endl;
            }
           else if (Calculate(NS, SP, SC, PP, PC) == 0)
          {
         cout<<"There is neither profit nor loss: " << endl;
        }
       else 
      {
     cout<<"The loss is $" <<Calculate(NS, SP, SC, PP, PC) << endl;
    }
   }
  // end of the program 
