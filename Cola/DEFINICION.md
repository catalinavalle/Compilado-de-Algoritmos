DEFINICION DE FILA O COLA
'''
struct Nodo {
	Tipo_dato info ;
	struct Nodo * sig ;
};
typedef struct Nodo tNodo ;
typedef tNodo * Fila ;
Fila CreaNodo ( Tipo_dato val1 ){
	Fila aux ;
	aux = ( Fila ) malloc ( sizeof ( tNodo ));
	SI ( aux != x NULL ) ENTONCES {
		aux - > info = val1 ;
		aux - > sgte = NULL ;
	}
	RETORNAR aux ;
}
Fila F = NULL ;
F = CreaNodo ( valor1 );
'''
