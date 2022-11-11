## Consultar elemento en posicion P

~~~
Tipo_dato ConsultaPosicion ( Lista L , Num p ) {
	Lista aux ;
	Num i;
	aux = L ;
	i = 1;
	MIENTRAS ( i < p ) HACER {
		aux = aux - > sig ;
		i = i +1;
	}
	RETORNAR aux -> info ;
}
~~~
