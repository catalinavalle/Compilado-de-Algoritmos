## Eliminar al principio

~~~
Tipo_dato * EliminarAlPrincipio ( Tipo_dato L[ n ]){
	Num i;
	i = 1;
	MIENTRAS (i > n) HACER {
		L[ i] = L[i +1];
		i = i +1; /* Avanza */
	}
	n = n -1;
	RETORNAR L;
}
~~~
