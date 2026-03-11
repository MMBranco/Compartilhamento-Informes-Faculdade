=================================================
import java.util.Arrays;

public class Bolha{
	public static void main (String args[] ){
	int vetor[] = {0,23,1,6,4,0,5,11};
	System.out.println(Arrays.toString(vetor));
	ordenar(vetor);
	System.out.println(Arrays.toString(vetor));
	
	}
	private static void ordenar(int vetor[]) {
		for(int i = 0; i<vetor.length -1; i++){
			for(int j = 0; j<vetor.length -1; j++){
				if(vetor[j] > vetor[j+1]){
					int aux = vetor[i];
					vetor[i] = vetor[i+1];
					vetor[i+1] = aux;
				}
			}
		}
		
	}
}
===============================================
import java.util.Scanner;

public class Main {

    public static int contarPalavras(String frase) {
		int tamanho = frase.length();
		return tamanho;
        
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String frase = sc.nextLine();

        System.out.println(contarPalavras(frase));
    }
}
=============================================================

import java.util.Scanner;

public class contasPalavras {

    public static int contarPalavras(String frase) {
        if (frase == null || frase.trim().isEmpty()) {
            return 0;
        }
        String[] palavras = frase.trim().split("\\s+");
        
        return palavras.length;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String frase = sc.nextLine();

        System.out.println(contarPalavras(frase));
        
        sc.close();
    }
=============================================================

public class Multiplos {

    public static int somaMultiplos3ou5(int n) {
        int soma = 0;

        for (int i = 0; i < n; i++) {
            if (i % 3 == 0 || i % 5 == 0) {
                soma += i; 
            }
        }

        return soma;
    }

    public static void main(String[] args) {
       
        System.out.println(somaMultiplos3ou5(10)); 
        System.out.println(somaMultiplos3ou5(20)); 
    }
}


}
===================================================================================


import java.util.Scanner;

public class Main {

    public static int contarConsoantes(String s) {
        int contador = 0;

        for (int i = 0; i < s.length(); i++) {
            char c = Character.toLowerCase(s.charAt(i));

            if (c != 'a' && c != 'e' && c != 'i' && c != 'o' && c != 'u' && c != ' ') {
                contador++;
            }
        }

        return contador;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String palavra = sc.nextLine();

        System.out.print(contarConsoantes(palavra));
    }
}

=================================================================

import java.util.Scanner;

public class Main {

    public static int produtoEscalar(int[] a, int[] b, int n) {
        int resultado = 0; 

        for (int i = 0; i < n; i++) {
            resultado += (a[i] * b[i]);
        }

        return resultado;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        int[] a = new int[n];
        int[] b = new int[n];

        for (int i = 0; i < n; i++) {
            a[i] = sc.nextInt();
        }

        for (int i = 0; i < n; i++) {
            b[i] = sc.nextInt();
        }

        System.out.print(produtoEscalar(a, b, n));
        
        sc.close();
    }
}

===============================================
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();
        
        int soma = 0;

        for (int i = a; i <= b; i++) {

            if (i % 2 == 0) {
                soma += i;
            }
        }

        System.out.println("A soma dos pares entre " + a + " e " + b + " é " + soma);
        
        sc.close();
    }
}


