## Eliminar elemento de posicion P

~~~
Lista EliminaListaPosicion ( Lista L , Num p ){
	Lista aux1 , aux2 ;
	Num i;
	aux1 = L;
	SI (p == 1) ENTONCES {
		L = L - > sig ;
		aux1 -> sig = NULL ;
		LiberaNodo ( aux1 );
	}
	SINO {
		i = 1;
		MIENTRAS (i < p - 1) HACER {
			aux1 = aux1 -> sig
			i = i +1;
		}
		aux2 = aux1 -> sig ;
		aux1 -> sig = aux2 - > sig ;
		aux2 -> sig = NULL ;
		LiberaNodo ( aux2 );
	}
	aux1 = NULL ;
	RETORNAR L;
}
~~~
