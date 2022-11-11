## Largo de la lista

~~~
Num LargoLista ( Lista L ){
	Lista aux ;
	Num cont ;
	cont = 0;
	aux = L ;
		MIENTRAS ( aux != NULL ) HACER 		{
			cont = cont +1;
			aux = aux - > sig ;
		}
	RETORNAR cont ;
}
~~~
