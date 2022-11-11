## Recorrido en profundidad

~~~
Void ProfundidadRec ( Num nodo ){
	Num i;
	Visitado [ nodo ] = VERDADERO ;
	ESCRIBIR ( nodo );
	i = 1;
	MIENTRAS (i <= n) HACER {
		SI (M [ nodo ,i] != 0) ENTONCES {
			SI ( NO ( Visitado [i ])) ENTONCES
				ProfundidadRec (i ); 
		}
		i = i + 1;
	}
}
~~~
