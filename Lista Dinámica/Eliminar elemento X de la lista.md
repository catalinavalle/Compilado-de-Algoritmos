## Eliminar elemento X de la lista

~~~
Lista EliminaValor ( Lista L , Tipo_dato x ){
	Lista aux1 , aux2 ;
	SI (L -> info == x ) ENTONCES {
		aux1 = L;
		L = L - > sig ;
		aux1 -> sig = NULL ;
		LiberaNodo ( aux1 );
	}
	SINO {
		aux1 = L;
		MIENTRAS ( aux1 - > info != x) 	HACER {	
			aux1 = aux1 -> sig ;
		}
		aux2 = L;
		MIENTRAS ( aux2 - > sig != aux1 ) HACER
			aux2 = aux2 -> sig ;
		}
		aux2 -> sig = aux1 - > sig ;
		aux1 -> sig = NULL ;
		LiberaNodo ( aux1 );
		aux1 = NULL ;
		aux2 = NULL ;
	}
	RETORNAR L;
}
~~~
