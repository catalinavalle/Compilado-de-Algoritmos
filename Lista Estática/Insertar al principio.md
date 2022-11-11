## INSERTAR AL PRINCIPIO

~~~
Tipo_dato  * InsertaAlPrincipio ( Tipo_dato L[n ], Tipo_dato X ){
	Num i;
	i = n +1;
	MIENTRAS (i > 1) HACER {
		L[ i] = L[i -1];
		i = i -1; /* Retrocede */
	}
	L [1] = X;
	n = n +1;
	RETORNAR L;
}
~~~
