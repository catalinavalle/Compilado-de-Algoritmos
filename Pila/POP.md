## POP: Extraer primer elemento de pila

~~~
Pila Pop ( Pila P ) {
	Pila pNodo ;
	SI ( P != NULL ) ENTONCES {
		pNodo = P ;
		P = P - > sig ;
		pNodo - > sig = NULL ;
		LiberaNodo ( pNodo );
	}
	RETORNAR P ;
}
~~~
