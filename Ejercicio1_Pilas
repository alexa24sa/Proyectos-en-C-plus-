/*Ejercicio 1: Hacer un programa para agregar números enteros a una pila, hasta que el usuario lo decida,
después mostrar todos los números introducidos en la pila.*/
#include<iostream>
#include<conio.h>

using namespace std;

//creamos una función global:
//realizamos la estrcutura de nodo:
	
	struct Nodo {
		int dato;//valor que estara contenido dentro del struct Nodo
		Nodo *siguiente; //apuntador al siguiente nodo
	};

void agregarPila(Nodo *&, int);//se le pasan los parámetros de nodo como puntero por referencia y el otro es el dato 
void sacarPila(Nodo *&, int &);

//Prototipo de Función
int main(){
	//llamamos al struct dentro del main principal para poderla usar como pila
	Nodo *pila  = NULL; //inicializamos un struct de tipo Nodo como apuntador de nombre pila con valor de cero
	int dato;
	char rpt;
	
	do{
		cout<<"Digite un número: ";
		cin>>dato;
		agregarPila(pila, dato);
		
		cout<<"\n Deseas agregar otro elemento a PILA(s/n): ";
		cin>>rpt;
		
	}while((rpt=='s')||(rpt=='S'));
	
	cout<<"\nSacando todos los elementos de la Pila: ";
	while(pila!=NULL){
	    sacarPila(pila, dato);
	    if(pila != NULL){
	        cout<<dato<< ", ";
	    } else {
	       cout<<dato<<".";
	    }
	    
	}
	
	
	getch ();
	return 0;
}

void agregarPila(Nodo *&pila, int n){
	Nodo  *nuevoNodo = new Nodo(); //reservamos memoria para un nuevo nodo
	nuevoNodo -> dato = n; /*guardar un nuevo elemento de la pila dentro del dato. Posteriormente
	se apunta a la variable de tipo "dato" dentro del struct y se almacenará en esta el valor de 
	la variable "n"*/
	nuevoNodo -> siguiente = pila; /*se comienza desde la pila para agregar apuntdando a la variable
	de tipo puntero llamada "siguiente" a la cuál se le asignará el valor de "pila" */
	pila = nuevoNodo; /*finalmente a "pila" se le asignará la dirección de memoria de nuevoNodo
	ya que dentro pila ya habrá un nuevo espacio en el que almacenar valores*/
	
	cout <<"\t Elemento "<<n<<" ha sido agregado a la pila correctamente";	
}


void sacarPila(Nodo *&pila, int &n){
    //Recordemos de la pila tiene una lógica de programación siguiente: LIFO
    Nodo *aux = pila; //a la variable auxiliar se le asigna el valor de la cima de la pila
    n = aux-> dato; /*"a la variable n se le asignará el último valor específico contenido dentro de "dato"
    es decir, que se le asigna la cima de la pila*/
    pila = aux -> siguiente; /*ahora a pila se le asigna el valor de la siguiente dirección de memoria
    , es decir irémos avanzando entre los elementos de la pila, y ahora pila se encontrará en la penúltima 
    posición*/
    delete aux; //eliminamos lo contenido dentro de la variable auxiliar 
}
