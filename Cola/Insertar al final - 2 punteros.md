## Insertar al final, 2 punteros. U apunta al ultimo elemento.
~~~
Fila InsertarFila ( Fila F , Fila U , Tipo_dato x) {
	Fila pNodo ;
	pNodo = CreaNodo (x );
	SI (F == NULL ) ENTONCES
		F = pNodo ;
	SINO
		U -> sig = pNodo ;
	U = pNodo ;
	pNodo = NULL ;
	RETORNAR F , U;
}
~~~
