## Localizar elemento

~~~
Num LocalizarElemento ( Lista L , Tipo_dato x) {
	Lista aux ;
	Num i;
	aux = L ;
	i = 1;
	MIENTRAS ( aux != NULL ) HACER {
		SI ( aux - > info == x ) ENTONCES
			RETORNAR i ;
		aux = aux - > sig ;
		i = i +1;
	}
	RETORNAR -1;
}
~~~
