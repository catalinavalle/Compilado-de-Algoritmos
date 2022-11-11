## Consultar posicion de elemento X

~~~
Num LocalizaElemento ( Tipo_dato L[n] , Tipo_datos X ){
	Num i;
	i =1;
	MIENTRAS (i <= n) HACER {
		SI (L [i] == X) ENTONCES {
			RETORNAR i;
		}
	i= i +1;
	}
	RETORNAR -1;
}
~~~
