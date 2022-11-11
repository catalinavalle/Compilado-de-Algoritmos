// Algoritmo de DIJKSTRA

- Permite encontrar los caminos de costo mínimo en grafos ponderados/valuados.
- Este FAMOSO algoritmo permite construir todos los caminos de costo
  mínimo desde un nodo que recibe como parámetro de entrada y el
  resto de los nodos de un grafo valuado.
- El grafo puede ser dirigido o no dirigido.
- El grafo puede ser no valuado: en este caso calcula el camino de largo
  menor (menor número de arcos).
- Los costos del grafo siempre deben ser positivos.

Implementación:
- Debe trabajar con alguna representación computacional de grafos: 
	- Matriz de costos.
- Para cada información asociada a los nodos:
	- Arreglo binario visitados
	- Arreglo de costos acumulados
	- Arreglo de nodos anteriores.

~~~

Conjunto Dijkstra (C : Matriz de costos de orden n , v0 : nodo origen ){
	BOOL Visitado [n ];
	Num CostoAcum [n] , NodoAnt [n ], i , j ;
	i = 1;
	MIENTRAS (i <= n) HACER {
		Visitado [i] = FALSO ;
		i = i + 1;
	}
	Visitado [ v0 ] = VERDADERO ;
	i = 1;
	MIENTRAS (i <= n) HACER {
		SI (C [ v0 ] , i) != 0) ENTONCES
			CostoAcum [i] = C[ v0 ][ i ];
		SINO
			CostoAcum [i] = infty ;
		NodoAnt [i] = v0 ;
		i = i + 1;
	}
	MIENTRAS NumeroNodosSinVisitar ( Visitados ) > 1 HACER {
		w = NodoMinimoCostoSinVisitar ( CostoAcum ); // Escoge w sin visitar con menor CostoAcum
		Visitado [w] = VERDADERO ;
		j = 1;
		MIENTRAS (j <= n) HACER {
			SI (( C [w , j] != 0) Y ( NO VISITADO [j ])) ENTONCES {
				SI ( CostoAcum [w] + C [w ,j ] < CostoAcum [j ]) ENTONCES {
					NodoAnt [j] = w;
					CostoAcum [j] = CostoAcum [w] + C [w ,j ];
				}
			}
			j= j + 1;
		}
	}
	RETORNAR NodoAnt , CostoAcum ;
}



Num NumeroNodosSinVisitar ( BOOL Visitados [n ]){
	Num i , cont ;
	i = 1;
	cont = 0;
	MIENTRAS (i <= n) HACER {
		SI ( NO Visitado [i ]) ENTONCES {
			cont = cont + 1;
		}
		i = i + 1;
	}
	RETORNAR cont ;
}


Num NodoMinimoCostoSinVisitar ( Num CostoAcum [n], BOOL Visitados [n ]) {
	Num i , nodo , minimo ;
	i = 1;
	MIENTRAS ( Visitados [i] == 0) HACER { // Primer nodo "i" sin visitar
		i = i + 1;
	}
	minimo = CostoAcum [i ]; //" minimo " inicializado en i
	nodo = i; // Inicializa " nodo " con la posicion del costo " minimo "
	i = i + 1;
	MIENTRAS (i <= n) HACER {
		SI ( NO ( Visitado [i ])) ENTONCES {
			SI ( CostoAcum [i] < minimo ) ENTONCES {
				minimo = CostoAcum [i ];
				nodo = i;
			}
		}
		i = i + 1;
	}
	RETORNAR nodo ;
}
~~~
