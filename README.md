// Parcial-Analisis-Numerico
//Punto 1
//********************************************************************************
void raices (int a, int b, int c){

    float x1,x2=0;
    float raiz=0;

    float r1 = pow(b,2);
    r1 = r1- (4*a*c);

    if(r1 < 0){
        r1=r1*-1;
        raiz = sqrt(r1);
        x1= (-b + raiz)/(2*a);
        x2= (-b - raiz)/(2*a);

        cout << "La raiz es compleja conjugada" << endl;
        cout << "Primera raiz: " << x1 << "i" << endl;
        cout << "Segunda raiz: " << x2 << "i" <<endl;

    }else{

        raiz = sqrt(r1);
        x1= (-b + raiz)/(2*a);
        x2= (-b - raiz)/(2*a);

        if(x1==(x2)){
            cout << "las raices son de multiplicidad 2" << endl;
        }else{
            cout << "La raiz es multiplicidad conjugada " << endl;
        }
        cout << "Primera raiz: " << x1 << endl;
        cout << "Segunda raiz: " << x2 << endl;
    }
}
//Punto 2b
//*********************************************************************************
#include <iostream>
#include <math.h>

using namespace std;
    long double funcion(long double x);
int main(){
    long double x0=1.5;
    long double x1=1;
    long double x2;
    long double tolerancia=0.0001;

    for(int i=0;i<5;i++){
        x2=x1-(funcion(x1))*((x1-x0)/(funcion(x1)-funcion(x0)));
        cout<<x2<<"\n";
        x0=x1;
        x1=x2;
    }
}
long double funcion(long double x){
    return exp2(x)-1.3;
}
//*********************************************************************************
//Punto 3c
 import math
def f1(x):
    return x**4-x
def f2(x):
  return 4*(x**3)-1


xn=0
x0=1
aux=0
tol=0.000001
error=1

while error>= tol:

    xn=x0-(f1(x0)/f2(x0))
    print (xn)
    error=(xn-x0)/xn
    x0=xn
//*********************************************************************************
//Punto 4
#include <iostream>
#include <math.h>

using namespace std;
    long double potencia(int b,int p);
    int factorial(int a);
int main(){
    int poten =0;
    long double result=0, respuesta;

    for(int i=0;i<8;i++){
        respuesta=potencia(-5,poten)/factorial(poten);
        result+=respuesta;
        cout<<result*-1<<endl;
        poten++;
    }
}
long double potencia(int b,int p){
    return pow(b,p);
}
int factorial(int a){
    int b,factorial;
    factorial=1;
    for (b=1 ; b<=a ; b++)
    {
         factorial=b*factorial;
    }
    return factorial;
}
