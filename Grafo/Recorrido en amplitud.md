## Recorrido en amplitud

~~~
Nada Amplitud (M: Matriz de Adyacencia orden n; v0 : nodo inicial ){
	Fila F;
	BOOL Visitado [n ]; // Todos los nodos inicialmente no visitados
	Num i , nodo ;
	F = InsertarAlFinal (v0 , F );
	MIENTRAS (F != VACIO ) HACER {
		nodo = EliminarPrimero (F );
		SI NO ( Visitado [ nodo ]) ENTONCES {
			Visitado [ nodo ] = VERDADERO ;
			ESCRIBIR ( nodo );
			i = 1;
			MIENTRAS (i <= n) HACER {
				SI (M [ nodo ,i] != 0) ENTONCES {
					SI NO ( Visitado [i ]) Y NO ( Esta ?(i , F )) ENTONCES {
						F = InsertarAlFinal (i , F );
					}
				}
				i = i + 1;
			}
		}
	}
}
~~~
