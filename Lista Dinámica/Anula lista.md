## Eliminar lista

~~~
Lista AnulaLista ( Lista L ){
	Lista aux ;
	MIENTRAS ( L != NULL ) HACER {
		aux = L ;
		L = L - > sig ;
		aux - > sig = NULL ;
		LiberaNodo ( aux );
	}
	RETORNAR L ;
}
~~~
