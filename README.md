package application;

import java.util.LinkedHashSet;
import java.util.Set;

public class Program {
	
	public static void main(String[] args) {
		
		Set<String> set = new LinkedHashSet<>();
		
		/*
		 * o HashSet ele não garante pra você a ordem do que foi escrito, ele vai ser estremamente rapido, só que ele vai
		 * ter essa desvantagem de não manter a ordem pra você, em muitos problemas a ordem pode não importar, então,
		 * se a ordem não importa, o HashSet é o mais indicado por ele ser mais rapido.
		 * 
		 * só pra mim ter uma ideia, eu posso trocar o HashSet pelo TreeSet, ai eu rodando o programa, o TreeSet ele vai
		 * ordenar os dados, ele mantem os dados ordenados na ordem alfabetica, no caso aqui é String, ele ordenou por 
		 * String.
		 * 
		 * o LinkedHashSet ele mantem a ordem em que os elementos foram inseridos, deferentemente do HashSet.
		 */
		
		set.add("TV");
		set.add("Notebook");
		set.add("Tablet");
		
		
		/*
		 * clear(): ele esvazia o conjunto.
		 * size(): que te retorna o tamanho do conjunto, a quantidade de elementos.
		 * removeIf(recebendo um predicado): ele vai remover do conjunto todo mundo que atender esse predicado aqui.
		 */
		//set.remove("Tablet");
		//set.removeIf(x -> x.length() >= 3);//(eu vou remover todo elemento X, tal que x.length() seja maior ou igual a 3.)
		set.removeIf(x -> x.charAt(0) == 'T');//(eu vou remover todo mundo que tenha a primeira letra igual a letra 'T'
		
		for (String p : set) {
			System.out.println(p);
		}
	}
}
