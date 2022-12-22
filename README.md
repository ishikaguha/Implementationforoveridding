# Implementationforoveridding
Explains the working of function overiding-  menu driven code which allows the user to choose from which account he/she/them wants to withdraw money from
#include <iostream>
using namespace std;
class salary
{
    public:
    char name[25];
    int id;
    int s;
    virtual void salary_cal()
    {
        cout<<"\nEnter the name of the employee = ";
        cin>>name;
        cout<<"\nEnter the id of the employee = ";
        cin>>id;
        cout<<"\nEnter the salary of the employee = ";
        cin>>s;
    }
};
class regular: public salary
{
    public:
    float da,hra;
    int bs;
    void salary_cal()
    {
        cout<<"\nEnter the basic salary of a regular employee = ";
        cin>>bs;
        da=(10*bs)/100;
        hra=(15*bs)/100;
        cout<<"\nSalary with 10percent DRA = "<<bs-da<<endl;
        cout<<"\nSalary with 10percent HRA = "<<bs-hra<<endl;
    }
};
class parttime: public salary
{
    public:
    int hr,p;
    void psalary_cal()
    {
        cout<<"\nENter the no. of hours = ";
        cin>>hr;
        cout<<"\nEnter pay per hour = ";
        cin>>p;
        cout<<"\nSalary of a part-time employee = "<<p*hr<<endl;
    }
};
int main()
{
    salary *ptr= new regular;
    ptr->salary_cal();
    parttime ob;
    ob.psalary_cal();
}
