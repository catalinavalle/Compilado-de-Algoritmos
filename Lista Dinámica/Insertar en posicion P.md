## Insertar en posición P

~~~
Lista InsertaEnPosicion ( Lista L , Tipo_dato x , Num p ){
	Lista pNodo , aux ;
	Num i , largo ;
	largo = LargoLista ( L );
	SI (p <= largo +1) ENTONCES { 
		pNodo = CreaNodo (x );
		SI (p == 1) ENTONCES {				
			pNodo -> sig = L;
			L = pNodo ;
		}
		SI NO {
			aux = L;
			i = 1;
			MIENTRAS (i < p - 1) HACER {
				aux = aux -> sig ; 
				i = i +1;
			}
			pNodo -> sig = aux - > sig ;
			aux -> sig = pNodo ;
			aux = NULL ;
		}
	}
	pNodo = NULL ;
	RETORNAR L;
}
~~~
