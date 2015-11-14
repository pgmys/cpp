# cpp
programy cpp
#include <iostream>
#include<iomanip>
using namespace std;


 int f_gorai(int x )
 {
    return (200+2*x*x-x)/200;
}

 int f_doli(int x )
 {
    return (x*x) / 50;
 }



 double f_gora(double x )
 {


    return (200+2*x*x-x)/200;
}

 double f_dol(double x )
 {


    return (x*x) / 50;
 }

int main()
{
    int i;
    double pole=0.0;
    double l=0.01;
    for(i=1; i<=1000; i++)
    {

        pole+=l*f_gora(i*l)+l*f_dol(i*l);


    }
    cout<<"odpowiedz do punktu a;"<<setprecision(4)<<pole<<endl;
    i=1;
    while( (f_gorai(i)+f_doli(i)<26) )
    {
i++;
        //cout<<i<<"  "<<f_gorai(i)+f_doli(i)<<"  "<<f_gorai(i)<<"teraz dol: "<< f_doli(i)<<endl;

    }
     cout<<"C= "<<i+100<<"  wspolrzedne "<<f_gorai(i)<<"  i  -"<<f_doli(i);
    return 0;
}
