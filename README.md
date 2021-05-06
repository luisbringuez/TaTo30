# TaTo30
practicafinal
calculadora class Calculadora
{
    public:
        Calculadora();
        /**Operaciones */
        long int Calcular_Factorial(int numero); // 1
        double Raiz_Cuadrada(int numero); // 2
        int Potencia(int numero, int potencia); // 3
        int Sumar_arreglo(int arreglo[], int tamanio); // 4
        int Restar_arreglo(int arreglo[], int tamanio); // 5
        double Multiplicar_arreglo(int arreglo[], int tamanio); // 6
        double Obtener_Promedio(int arreglo[], int tamanio); // 7
        std::string Binomio_suma_cuadrado(int a, int b); // 8
        std::string Binomio_resta_cuadrado(int a, int b); // 9
        std::string Binomio_suma_cubo(int a, int b); // 10
        std::string Binomio_resta_cubo(int a, int b); // 11
        double * Obtener_raices_ecuacion_cuadratica(int a, int b, int c); // 12
        double Logaritmo(int base, double numero); // 13
        double Calcular_Seno(double x); //14
        double Calcular_Coseno(double x); //15
        double Calcular_Tangente(double x); //16

        ~Calculadora();

    protected:

    private:
        const double PI = 3.14159;
        const double EPSILON = 0.00001;
        double Loga(double x,int i);
        double Seno(double x);
        double angulos_a_radianes(double angulo);
        double positivo(double numero);
        double Potencia(double base, int exp);
        long int Factorial(int factor);
        double Pot(double base, int exp);
        long int Fac(int factor);
        double Coseno(double x);
        double Tangente(double x);
};

#endif // CALCULADORA_H
