package application;

import java.util.Arrays;
import java.util.Set;
import java.util.TreeSet;

public class Program {
	public static void main(String[] args) {
		
		Set<Integer> a = new TreeSet<>(Arrays.asList(0, 2, 4, 5, 6, 8, 10));
		Set<Integer> b = new TreeSet<>(Arrays.asList(5, 6, 7, 8, 9, 10));
		
		//union
		/*
		 *eu vou criar um terceiro conjunto C, e aqui eu to usando um construtor especial que eu passo uma outra coleção(a)
		 *como argumento, no casso então aqui eu to criando o conjunto C, que vai ser uma cópia do conjunto (a).
		 *depois eu chamo c.addAll(b);, em outras palavras eu estou fazendo a união desse conjunto C com o conjunto B.
		 */
		Set<Integer> c = new TreeSet<>(a);
		c.addAll(b);
		System.out.println(c);
		
		//intersection
		/*
		 * depois eu vou fazer denovo a instanciação do quarto conjunto D, como uma copia do conjunto A, e eu vou chamar a 
		 * intersecção.
		 * d.retainAll(b);, ou seja, em outras palavras, são somente aqueles elementos que tem em comum nos conjuntos
		 */
		Set<Integer> d = new TreeSet<>(a);
		d.retainAll(b);
		System.out.println(d);
		
		//difference
		/*
		 * eu vou criar um quinto conjunto E, que vai ser a copia do conjunto A, e ai eu vou fazer a diferença, eu vou 
		 * remover do conjunto E, todo mundo que ta no conjunto B.
		 */
		Set<Integer> e = new TreeSet<>(a);
		e.removeAll(b);
		System.out.println(e);
	}
}
