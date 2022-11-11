## Crea nodo

~~~
Lista CreaNodo ( val1 , ... , valn ){
	Lista aux ;
	aux = ( Lista ) malloc ( sizeof ( tNodo ));
	SI ( aux != NULL ) ENTONCES {
		aux - > campo1 = val1 ;
		...
		aux - > campon = valn ;
		aux - > sig = NULL ;
	}
	RETORNAR aux ;
}

Lista L = NULL ;
L = CreaNodo ( val1 , ... , valn );
~~~
