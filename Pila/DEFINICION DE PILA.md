## DEFINICION DE PILA

~~~
struct Nodo {
	Tipo_dato info ;
	struct Nodo * sig ;
};
typedef struct Nodo tNodo ;
typedef tNodo * Pila ;
Pila CreaNodo ( Tipo_dato val1 ){
	Pila aux ;
	aux = ( Pila ) malloc ( sizeof ( tNodo ));
	SI ( aux != NULL ) ENTONCES {
		aux - > info = val1 ;
		aux - > sgte = NULL ;
	}
	RETORNAR aux ;
}
Pila P = NULL ;
P = CreaNodo ( valor1 );
~~~
