//LENGUAJE C
//ACTIVIDAD COMPLEMENTARIA #1

//librerias
#include <stdio.h>
#include <stdlib.h>
#include <iostream>
#include <string.h>
#include <time.h>

using namespace std;
//Funcion principal

int main()
{
	
		//Variables
	int N,Al,des=0,contador=0,i=0; // N =variable del numero que ingresa el usuario ,Al =numero aleatorio ,des= la decicion de empezar de nuevo 
	srand(time(NULL));
	char  nombre[100]={0};

    cout<<"Hoy jugaremos Adivina El Numero"<<endl;
	cout<<"Debes escribir un numero del 1-100, cuando aciertes"<<endl<<"el programa dejara de pedirte el numero y te mostrara"<<endl;
	cout<<"el numero de intentos"<<endl<<"BUENA SUERTE"<<endl;         
	cout<<"___________________________________________________________________________________________________________________"<<endl<<endl;      	
                    	
                do{
                	    cout<<"_____________Lenguaje C _______________"<<'\n'<<"          ACTIVIDAD COMPLEMENTARIA 1           "<<"\n";
                        cout<<"\n"<<"Elizabeth Perez Valderrama"<<"\n"<<"\n";
                	
                	Al= 1+ rand()%(101-1); //estamos pidiendole al programa un numero aleatorio entre 1-100
                    cout<<"Hola, Cual es tu nombre"<<endl;
					cin.getline(nombre,100,'\n'); //almacena la cadena y le da un valor maximo de 100 espacios
			
                	do 
                    {
                    	cout<<"Hola "<<nombre<<'\n'<<"  Escribe un numero 1-100"<<endl;
                    	cin >>N;
                    	
                    	if(N<0 ||N>100)  //condicion de numeros entre 0-100
                    	{
                    		cout<<"Error!"<<"\t"<<"Escribe un numero entre 0-100"<<endl;
						}
                    	
                    	if (N<Al)//le muestra al usuario que el numero que escribio es menor al numero a adivinar
                    	{
                    		cout<<"NO!"<<"\t"<<"Escribe un numero mas grande"<<endl;
						}
						else if(N>Al) //Le muestra al usuario que el numero que escribio es mayour a al numero a adivinar
						{
							cout<<"NO!"<<"\t"<<"Escribe un numero mas pequeño"<<endl;
						}		        
                    	contador++;//aumenta el contador en uno cada ves que el numero escrito por el usuario no sea correcto
				    	}
					while(N!=Al);
					    cout<<"-------------------------------------------------------------------------------"<<endl;
                    	cout<<"Felicidades has acertado"<<endl<<endl;
					    cout<<"Tu numero de intentos es :"<<"\t"<<contador<<endl;//muestra el numero de intentos
                    	cout <<"quieres empezar de nuevo?"<<endl<<"1) si"<<"\t"<<"2) salir del juego"<<endl;	//El programa da la opcion de empezar de nuevo o finalizar el juego 
						cin>>des;
						system("cls");
				}    	
				while(des!=2);
                    	
         	system("cls");

	cout<<"EL JUEGO HA FINALIZADO"<<"\n";cout<<"Chao "<<nombre<<endl;
	system("pause");
	return 0;
}
