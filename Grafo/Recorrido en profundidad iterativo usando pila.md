## Recorrido en profundidad iterativo usando pila

~~~
Nada ProfIter (M[n]; nodo inicial){
	Pila P;
	BOOL Visitado [n ]; // Todos los nodos inicialmente no visitados
	Num i , nodo ;
	P = Push (v0 , P );
	MIENTRAS (P != VACIO ) HACER {
		nodo = Pop (P );
		SI NO ( Visitado [ nodo ]) ENTONCES {
			Visitado [ nodo ] = VERDADERO ;
			ESCRIBIR ( nodo );
			i = n;
			MIENTRAS (i >= 1) HACER {
				SI (M [ nodo ,i] != 0) ENTONCES {
					SI NO(Visitado[i]) Y NO Esta?(i,P)) ENTONCES {
						P = Push(i, P);
					}	
				}
				i = i - 1;
			}
		}
	}
}
~~~
