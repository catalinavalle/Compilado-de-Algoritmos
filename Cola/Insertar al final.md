## Insertar al final
~~~
Fila InsertarFila ( Fila F , Tipo_dato x) {
	Fila pNodo , aux ;
	pNodo = CreaNodo ( x );
	SI ( F == NULL ) ENTONCES
		F = pNodo ;
	SINO {
		aux = F ;
		MIENTRAS ( aux - > sig != NULL ) HACER
			aux = aux - > sig ;
		aux - > sig = pNodo ;
		aux = NULL ;
	}
	pNodo = NULL ;
	RETORNAR F ;
}
~~~
