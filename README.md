# vigilant-happiness
Use member functions to input the marks for each class. Identify a concept and write a function that can accept data members of both the classes and calculate the results.  Same function will print the result and total marks subject wise.    

#include <iostream> 
using namespace std; 
class External1; 
class Internal1 
{ 
    int math,oop,se,dsa; 
    public: 
    void readdata() 
    { 
        cout <<" Enter Math Internals "<<endl; 
        cin >>math; 
        cout <<" Enter OOP Internals "<<endl; 
        cin >>oop; 
        cout <<" Enter SE Internals "<<endl; 
        cin >>se; 
        cout <<" Enter DSA Internals "<<endl; 
        cin >>dsa; 
    } 
    friend void sum(Internal1 I1, External1 E1 ); 
}; 
class External1 
{ 
      int math,oop,se,dsa; 
    public: 
    void readdata() 
    { 
        cout <<" Enter Math Externals "<<endl; 
        cin >>math; 
        cout <<" Enter opp Externals "<<endl; 
        cin >>oop; 
        cout <<" Enter se Externals "<<endl; 
        cin >>se; 
        cout <<" Enter ds Externals "<<endl; 
        cin >>dsa; 
    } 
    friend void sum(Internal1 I1,External1 E1 ); 
}; 
 
void sum(Internal1 I1,External1 E1) 
{ 
    int s,s1,s2,s3; 
    s=I1.math+E1.math; 
    cout<<"Total Math marks :"<<s<<endl; 
    s1=I1.oop+E1.oop; 
    cout<<"Total OOP marks :"<<s1<<endl; 
    s2=I1.se+E1.se; 
    cout<<"Total SE marks :"<<s2<<endl; 
    s3=I1.dsa+E1.dsa; 
    cout<<"Total DSA marks :"<<s3<<endl; 
} 
 
int main() 
{ 
    Internal1 INTERNS; 
    INTERNS.readdata(); 
    External1 EXTERN; 
    EXTERN.readdata(); 
    sum(INTERNS,EXTERN); 
    return 0; 
}
