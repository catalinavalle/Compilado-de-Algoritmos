## Algoritmo de KRUSKAL

### Definición:
- Permite encontrar el Árbol de Cobertura Mínimo (ACM) en un grafo
  ponderado/valuado. Es decir, El camino más corto y a su vez "barato"
  para abarcar todos los nodos del grafo.
  
- La solución siempre es (n-1), siendo n la cantidad de nodos.

~~~
Conjunto Kruskal (G(V , A ): Grafo valuado conexo no dirigido ){
	T = VACIO ; // Lista de aristas que forman al ACM ( Salida )
	VS = VACIO ; // Conjunto de subconjuntos de vertices
	Q = Lista de aristas ordenadas segun costo de menor a mayor
	PARA CADA v EN V HACER {
		VS = Insertar ({ v} , VS );
	}
	MIENTRAS (| VS | > 1 Y Q != VACIO ) HACER {
		(u ,v) = Sacar del principio de Q ;
		SI (u EN W1 ) Y (v EN W2 ) Y ( W1 != W2 ) ENTONCES {
			Reemplazar en VS : W1 y W2 por W1 U W2 ;
			T = Insertar ((u ,v ), T );
		}
	}
	RETORNAR T;
}


Conjunto Kruskal (G(V , A ): Grafo valuado conexo no dirigido ){
	T = VACIO ; // Lista de aristas que forman al ACM ( Salida )
	VS = VACIO ; // Conjunto de subconjuntos de vertices
	Q = Lista de aristas ordenadas segun costo de menor a mayor
	PARA CADA v EN V HACER {
		VS = Insertar ({ v} , VS );
	}
	MIENTRAS (| VS | > 1 Y Q != VACIO ) HACER {
		(u ,v) = Sacar del principio de Q ;
		W1 = HallarConjunto (u );
		W2 = HallarConjunto (v );
		SI ( W1 != W2 ) ENTONCES {
			Reemplazar en VS : W1 y W2 por W1 U W2 ;
			T = Insertar ((u ,v ), T );
		}
	}
	RETORNAR T;
}
~~~
