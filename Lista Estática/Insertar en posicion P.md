## Insertar en posicion P

~~~
Tipo_dato * InsertaEnPosicionP ( Tipo_dato L[n ], Tipo_dato X , Num p ){
	Num i;
	i = n +1;
	MIENTRAS (i > p) HACER {
		L[ i] = L[i -1];
		i = i -1;   /* Retrocede */
	}
	L[ p] = X;
	n = n +1;
	RETORNAR L;
}
~~~
