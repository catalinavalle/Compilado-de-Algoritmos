## PUSH: Insertar al principio

~~~
Pila Push ( Pila P , Tipo_dato x ) {
	Pila pNodo ;
	pNodo = CreaNodo ( x );
	pNodo - > sig = P ;
	P = pNodo ;
	pNodo = NULL ;
	RETORNAR P ;
}
~~~
