## Insertar al final

~~~
Lista InsertarFinal ( Lista L , Tipo_dato x ){
Lista pNodo , aux ;
	pNodo = CreaNodo (x );
	SI (L == NULL ) ENTONCES
		L = pNodo ;
	SI NO {
		aux = L;
	MIENTRAS ( aux -> sig != NULL ) HACER
		aux = aux -> sig ;
		aux -> sig = pNodo ;
		aux = NULL ;
	}
	pNodo = NULL ;
}
~~~
