## Insertar al principio

~~~
Lista InsertarPrincipio ( Lista L , Tipo_dato x) {
	Lista pNodo ;
	pNodo = CreaNodo (x );
	pNodo - > sig = L;
	L = pNodo ;
	pNodo = NULL ;
RETORNAR L;
}
~~~
