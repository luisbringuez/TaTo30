# TaTo30
practicafinal
```c
#include "Calculadora.h"

using namespace std;

Calculadora::Calculadora(){
    //ctor
}

Calculadora::~Calculadora(){
    //dtor
}

//metodo 1
/**Metodo que calcula el factorial de un numero*/
long int Calculadora::Calcular_Factorial(int numero){
    long int resultado = 0;
    string cadena = "El factorial de ";
    cadena = cadena + std::to_string(numero) + " es : ";
    resultado = Factorial(numero);
    cadena = cadena + std::to_string(resultado);
    cout<<cadena<<endl;
    return resultado;
}

//metodo 2
double Calculadora::Raiz_Cuadrada(int numero){
    double temporal, raiz;
    raiz = numero / 2;
    temporal = 0;

    while(raiz != temporal){
        temporal = raiz;
        raiz = ( numero/temporal + temporal) / 2;
    }
    raiz = trunc( raiz * 100 ) / 100.0f ;
    cout<<"La raiz cuadrada de "<< numero<<" es: "<<raiz<<endl;
    return raiz;
}

//metodo 3
int Calculadora::Potencia(int numero, int potencia){
    int resultado = 1;
    if(numero>0){
        for(int i=0; i < potencia; i++){
            resultado = resultado * numero;
        }
        cout<<"El resultado de la potencia "<< numero <<"^"<<potencia<<" es: "<<resultado<<endl;
        return resultado;
    }
    else{
        cout<<"La potencia de 0 es 0"<<endl;
        return 0;
    }
}

//metodo 4
/** este metodo obtiene el resultado de sumar los valores almacenados en un vector entre si*/
int Calculadora::Sumar_arreglo(int arreglo[], int tamanio){
    int resultado = 0;
    for(int i=0; i< tamanio; i++){
        resultado = resultado + arreglo[i];
    }
    cout << "Suma de elementos de arreglo = " << resultado << endl;
    return resultado;
}

//metodo 5
/** este metodo obtiene el resultado de restar los valores almacenados en un vector entre si*/
int Calculadora::Restar_arreglo(int arreglo[], int tamanio){
    int resultado = 0;
    for(int i=0; i< tamanio; i++){
        resultado = resultado - arreglo[i];
    }
    cout << "Resta de elementos de arreglo = " << resultado << endl;
    return resultado;
}

//metodo 6
/** este metodo obtiene el resultado de multiplicar los valores almacenados en un vector entre si*/
double Calculadora::Multiplicar_arreglo(int arreglo[], int tamanio){
    double resultado = 1;
    for(int i=0; i< tamanio; i++){
        resultado = resultado * arreglo[i];
    }
    cout << "Multiplicacion de elementos de arreglo = " << resultado << endl;
    return resultado;
}

//metodo 7
/** este metodo obtiene el promedio de los valores almacenados en un vector*/
double Calculadora::Obtener_Promedio(int arreglo[], int tamanio){
    double resultado = 0.00;
    for(int i=0; i< tamanio; i++){
        resultado = resultado + arreglo[i];
    }
    resultado = resultado / tamanio;
    resultado = trunc( resultado * 100 ) / 100.0f ;
    cout << "Promedio de elementos del arreglo = " << resultado << endl;
    return resultado;
}

//metodo 8
/** este metodo resuelve un binomio de la forma (ax + b)^2 */
string Calculadora::Binomio_suma_cuadrado(int a,  int b){
    string resultado = "";
    string cadena = "Resolviendo: ";
    int coeficiente_a = 0;
    int coeficiente_b = 0;
    int coeficiente_c = 0;
    cadena = cadena + "(" + std::to_string(a)+"X + "+std::to_string(b)+")^2 ";
    coeficiente_a = a*a;
    coeficiente_b = 2*a*b;
    coeficiente_c = b*b;
    resultado = std::to_string(coeficiente_a) + "X^2 + " + std::to_string(coeficiente_b) + "X + " + std::to_string(coeficiente_c);
    cout<<cadena<<" = ";
    cout<<resultado<<endl;
    return resultado;
}

//metodo 9
/** este metodo resuelve un binomio de la forma (ax - b)^2 */
string Calculadora::Binomio_resta_cuadrado(int a, int b){
    string resultado = "";
    string cadena = "Resolviendo: ";
    int coeficiente_a = 0;
    int coeficiente_b = 0;
    int coeficiente_c = 0;
    cadena = cadena + "(" + std::to_string(a)+"X - "+std::to_string(b)+")^2 ";
    coeficiente_a = a*a;
    coeficiente_b = 2*a*b;
    coeficiente_c = b*b;
    resultado = std::to_string(coeficiente_a) + "X^2 - " + std::to_string(coeficiente_b) + "X + " + std::to_string(coeficiente_c);
    cout<<cadena<<" = ";
    cout<<resultado<<endl;
    return resultado;
}

//metodo 10
/** este metodo resuelve un binomio de la forma (ax + b)^3 */
string Calculadora::Binomio_suma_cubo(int a, int b){
    string resultado = "";
    string cadena = "Resolviendo: ";
    int coeficiente_a = 0;
    int coeficiente_b = 0;
    int coeficiente_c = 0;
    int coeficiente_d = 0;
    cadena = cadena + "(" + std::to_string(a)+"X + "+std::to_string(b)+")^3 ";
    coeficiente_a = a*a*a;
    coeficiente_b = 3*a*a*b;
    coeficiente_c = 3*a*b*b;
    coeficiente_d = b*b*b;

    resultado = std::to_string(coeficiente_a) + "X^3 + " + std::to_string(coeficiente_b) + "X^2 + " + std::to_string(coeficiente_c) + "X + "  + std::to_string(coeficiente_d);
    cout<<cadena<<" = ";
    cout<<resultado<<endl;
    return resultado;
}

//metodo 111
/** este metodo resuelve un binomio de la forma (ax - b)^3 */
string Calculadora::Binomio_resta_cubo(int a, int b){
    string resultado = "";
    string cadena = "Resolviendo: ";
    int coeficiente_a = 0;
    int coeficiente_b = 0;
    int coeficiente_c = 0;
    int coeficiente_d = 0;
    cadena = cadena + "(" + std::to_string(a)+"X - "+std::to_string(b)+")^3 ";
    coeficiente_a = a*a*a;
    coeficiente_b = 3*a*a*b;
    coeficiente_c = 3*a*b*b;
    coeficiente_d = b*b*b;

    resultado = std::to_string(coeficiente_a) + "X^3 - " + std::to_string(coeficiente_b) + "X^2 + " + std::to_string(coeficiente_c) + "X - "  + std::to_string(coeficiente_d);
    cout<<cadena<<" = ";
    cout<<resultado<<endl;
    return resultado;
}

//metodo 12
/** este metodo obtiene las raices de un polinomio cuadradico, usando la formula cuadratica*/
double * Calculadora::Obtener_raices_ecuacion_cuadratica(int a, int b, int c){
    double raices [2];
    string signo = "";
    string cadena = "Las raices del polinomio: ";
    double X1 = 0.00, X2 = 0.00;
    X1 = (-1* b + sqrt(b*b - 4*a*c))/2*a;
    X2 = (-1* b - sqrt(b*b - 4*a*c))/2*a;
    X1 = trunc( X1 * 100 ) / 100.0f ;
    X2 = trunc( X2 * 100 ) / 100.0f ;
    raices[0] = X1;
    raices[1] = X2;

    if(b>=0){
        signo = "+ ";
    }
    else{
        signo = "- ";
    }
    cadena = cadena + std::to_string(a) + "X^2 "+signo + std::to_string(b) + "X ";
    if(c>=0){
        signo = "+ ";
    }
    else{
        signo = "- ";
    }
    cadena = cadena + signo + std::to_string(c) + " son: ";

    cout<<cadena<<endl;
    cout<<"Raiz 1 = "<<X1<<endl;
    cout<<"Raiz 2 = "<<X2<<endl;

    return raices;
}

//metodo 13
double Calculadora::Logaritmo(int base, double numero) {
    double valor = 0;
    double temp1, temp2;
    temp1 = base;
    temp2 = numero;
    double resultado = 0;
    int i , presicion  = 10, repeticiones = 0;
    while(numero != 1 && presicion>=0) {
        for(i=0;numero>=base;i++) numero /= base;
            numero = Loga(numero,10);
            valor = 10*(valor + i);
            presicion--; repeticiones++;
    }
    resultado = (double)valor / Loga(10,repeticiones);
    cout<<"El Resultado del logaritmo log"<< temp1 << "("<<temp2<<") es: "<< resultado<<endl;
    return resultado;
}

double Calculadora::Loga(double x,int i) {
    double r = 1.0;
    for(i;i>0;i--) r *= x;
    return r;
}

//14
double Calculadora::Calcular_Seno(double x){
    double temp = x;
    double res = angulos_a_radianes(x);
    cout.precision(5);
    res = Seno(res);

    //res = trunc( res * 10000) / 10000.0f ;
    temp = angulos_a_radianes(x);
    cout<<"Los "<<x<<" grados convertidos a radianes son: "<<temp<<endl;
    cout<<"EL SENO de: "<< temp <<" radianes  es: "<<res<<endl;
    return res;
}

/**seno, con x en radianes usando series de taylor*/
double Calculadora::Seno(double x){
	double resultado=0;
	double resultado_anterior=0;
	int sumador = 0;
	//hacemos mientras la diferencia sea menor a la precisión que estamos buscando
	do{
		//almacenamos el resultado anterior
		resultado_anterior = resultado;
		//la serie de taylor
		resultado+= Pot(-1,sumador)*Pot(x,2*sumador+1)/Fac(2*sumador+1);
		sumador++;

	}while(positivo(resultado-resultado_anterior) >= EPSILON);
	return resultado;
}

//metodo 15
double Calculadora::Calcular_Coseno(double x){
    double temp = x;
    double res = angulos_a_radianes(x);
    cout.precision(5);
    res = Coseno(res);
    temp = angulos_a_radianes(x);
    //res = trunc( res * 10000) / 10000.0f ;
    cout<<"Los "<<x<<" grados convertidos a radianes son: "<<temp<<endl;
    cout<<"EL COSENO de: "<< temp <<" radianes  es: "<<res<<endl;
    return res;
}

/**coseno, con x en radianes usando series de taylor*/
double Calculadora::Coseno(double x){
	double resultado=0;
	double resultado_anterior=0;
	int sumador = 0;
	//hacemos mientras la diferencia sea menor a la precisión
	do{
		//almacenamos el resultado anterior
		resultado_anterior = resultado;
		//la serie de taylor
		resultado+= Pot(-1,sumador)*Pot(x,2*sumador)/Fac(2*sumador);
		sumador++;

	}while(positivo(resultado-resultado_anterior) >= EPSILON);
	return resultado;
}

double Calculadora::angulos_a_radianes(double angulo) {
	return (angulo * PI) / 180;
}

double Calculadora::positivo(double numero){
	if(numero<0) return -1*numero;
	return numero;
}

double Calculadora::Potencia(double base, int exp) {
	if(exp == 0 || base == 1){return 1;}
	if(base == -1){return 1-(exp%2)*2;}
	double resultado = base;
	while(exp-- > 1){
		resultado*=base;
	}
	return resultado;
}

long int Calculadora::Factorial(int factor){
	if(factor == 0) return 1;
	long int resultado = 1;
	do{
		resultado*=factor;
	}while(factor-- > 1);
	return resultado;
}

double Calculadora::Pot(double base, int exp) {
	if(exp == 0 || base == 1){return 1;}
	if(base == -1){return 1-(exp%2)*2;}
	double resultado = base;
	while(exp-- > 1){
		resultado*=base;
	}
	return resultado;
}

long int Calculadora::Fac(int factor){
	if(factor == 0) return 1;
	long int resultado = 1;
	do{
		resultado*=factor;
	}while(factor-- > 1);
	return resultado;
}

double Calculadora::Calcular_Tangente(double x){
    double temp = x;
    double res = angulos_a_radianes(x);
    cout.precision(5);
    res = Tangente(res);
    temp = angulos_a_radianes(x);
    cout<<"Los "<<x<<" grados convertidos a radianes son: "<<temp<<endl;
    cout<<"La tangente de: "<< temp <<" radianes  es: "<<res<<endl;
    return res;
}

/**Acá no usamos la serie de taylor porque es bastante grande pero asumimos que tangente = seno / coseno */
double Calculadora::Tangente(double x){
	if(x/(PI/2)== (int)(x/(PI/2))){
		cout << "Error: el angulo no debe ser multiplo de 90" << endl;
		return 0;
	}
	return Seno(x)/Coseno(x);
}


```

