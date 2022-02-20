package application;

import java.util.HashSet;
import java.util.Scanner;
import java.util.Set;

public class Program {

	public static void main(String[] args) {

		Scanner sc = new Scanner(System.in);

		Set<Integer> a = new HashSet<>();
		Set<Integer> b = new HashSet<>();
		Set<Integer> c = new HashSet<>();

		System.out.print("How many studends for course A? ");
		int number = sc.nextInt();
		for (int i = 0; i < number; i++) {
			int n = sc.nextInt();
			a.add(n);
		}

		System.out.print("How many studends for course A? ");
		number = sc.nextInt();
		for (int i = 0; i < number; i++) {
			int n = sc.nextInt();
			b.add(n);
		}

		System.out.print("How many studends for course A? ");
		number = sc.nextInt();
		for (int i = 0; i < number; i++) {
			int n = sc.nextInt();
			c.add(n);
		}
		
		Set<Integer> total = new HashSet<>(a);
		total.addAll(b);
		total.addAll(c);
		
		System.out.println("Total studends: " + total.size());
		
		sc.close();
	}

}

![set-exercicio-de-fixação-FOTO](https://user-images.githubusercontent.com/61166475/154861817-a2f3da57-cb57-490d-9a7c-7da31ed034fd.png)
