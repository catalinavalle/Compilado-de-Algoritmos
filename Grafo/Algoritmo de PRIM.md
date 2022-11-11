## Algoritmo de Prim

- Permite encontrar el Árbol de Cobertura Mínimo (ACM) en un grafo
ponderado/valuado.
	Permite encontrar aquel árbol, subgrafo del inicial (debe poseer todos
	los nodos), que sea de costo mínimo.

~~~
Conjunto Prim (G (V , A ): Grafo valuado conexo no dirigido ){
	T = VACIO ; // Lista de aristas que forman al ACM ( Salida )
	N = { Escoger cualquier vertice de V}
	MIENTRAS (N != V) HACER {
		(u ,v) = Arco de costo minimo en A con u en N o v en N , pero no ambos ;
		N = N U { x }; //x es el nodo u o v que no estaba en N
		T = T U {(u ,v )};
	}
	RETORNAR T;
}
~~~
