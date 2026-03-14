aula 27/02
import javax.swing.JOptionPane;
public class Tabuada{
	
public static void main(String [] args){
	int numero = Integer.parseInt(JOptionPane.showInputDialog("Diga o número para ser feito a sua tabuada"));
	System.out.println("Tabuada do " + numero);
	for( int tab= 0 ; tab <= 10; tab++){
		int result = tab * numero;
		System.out.println(tab + "x"  + numero + "=" + result);
	}
}
}
---------------------------------------------------------------------------------
import javax.swing.JOptionPane;
public class Plim {
	
	public static int funcao (String msg){
		System.out.println();
		return 0;
		
	}
	
	public static void main(String [] args){
		int numI = Integer.parseInt(JOptionPane.showInputDialog("Diga o numero inicial:"));
		int numF = Integer.parseInt(JOptionPane.showInputDialog("Diga o numero final:"));
		int numP = Integer.parseInt(JOptionPane.showInputDialog("Diga o numero Plim:"));
		for( int i = numI; i <= numF; i++){
			if(i%numP == 0){
				System.out.println("Plim");
			}else{
				System.out.println(i);
			}
		}
	}
}
---------------------------------------------------------------------------------------
import javax.swing.JOptionPane;

public class Plim {
  
    public static int lerNum(String mensagem) {
        return Integer.parseInt(JOptionPane.showInputDialog(mensagem));
    }

    public static void exePlim(int inicio, int fim, int plim) {

        for (int i = inicio; i <= fim; i++) {
            if (i % plim == 0) {
                System.out.println("Plim");
            } else {
                System.out.println(i);
            }
        }
    }

    public static void main(String[] args) {

        int numI = lerNum("Diga o numero inicial:");
        int numF = lerNum("Diga o numero final:");
        int numP = lerNum("Diga o numero Plim:");

        exePlim(numI, numF, numP);
    }
}
---------------------------------
import javax.swing.JOptionPane;
public class Num {
	public static void main(String [] args){
		 int maior = 0;
		 int menor = 9999999999;
		 int soma = 0 ;
		 int media = 0;
		for(int i = 1; i <= 5; i++){
		     int num = Integer.parseInt(JOptionPane.showInputDialog("Diga o numero:"));
			 if(maior<num){
				 maior = num;
			 }
			 if(menor<num){
				 menor = num;
			 }
			 soma += num;
			 int media = soma/5;
		}
	    System.out.println(maior);
		System.out.println(menor);
		System.out.println(media);
		
	}
	
}	


====================================================

import javax.swing.JOptionPane;

class Pessoa{
	String nome;
	int idade;
	String profissao;
	
	public void adicionaInfo(String n, int id, String pf){
		this.nome = n;
		this.idade = id;
		this.profissao = pf;
		
	}
	
	public void mostreInfo(){
		System.out.println("nome:"+ this.nome+ ", idade:" + this.idade+ ",Profissao: "+ this.profissao+ "Ano de nascimento: " + (2026 - this.idade) );
		
	}
}

public class Num {
	public static void main(String [] args){
	   Pessoa tmp;
	   tmp = new Pessoa();
	   Pessoa p2  = new Pessoa();
	   
	   tmp.adicionaInfo("Marcelo",35,"professor");
	   p2.adicionaInfo("João",45,"lenhador");
	   
	   tmp.mostreInfo();


	   p2.mostreInfo();
	}

}


(Aula dia 13/03 - códigos )

=========================================================================================
import java.util.Scanner


public class Num{
	public static void main(String args[]){
		
		int idades[] = {11,22,33,44,55};
		int maior = idades[0];
		for(int i = 0; i < idades.length; i++){
			
		}
		for (int i = 0; i<idades.length; i++){
		    System.out.println("Idades --->"+ idades[i]);
	        if (idades[i] > maior){
				maior = idades[i];
			System.out.println("Maior" + maior);
		    }
		}
	}
}

================================================================================================

import java.util.Scanner;
public class Num{
	
	public static int []lerVetor(int idades[]){
		Scanner sc = new Scanner(System.in);
		
		for(int i = 0; i < idades.length; i++){
			System.out.print("Digite sua idade: ");
            idades[i] = sc.nextInt();
		}
		for (int i = 0; i<idades.length; i++){
		    System.out.println("Idades --->"+ idades[i]);
	    }
		
	sc.close();   
	return idades;	
	}

	
	public static int maiorNum(int idades[]){
	int maior = idades[0];	
	for (int i = 0; i<idades.length; i++){
	        if (idades[i] > maior){
				maior = idades[i];
			}	
		}	
	return maior;	
	}
	
	
	public static void main(String args[]){
	   int idades[] = {0,0,0,0};
	   lerVetor(idades);
	
	int maior = maiorNum(idades);
        System.out.println("Maior idade: " + maior);
	
	}
	
}

==============================================================================================================
import java.util.Scanner;

class Auxiliar{
	
	public static int []lerVetor(int idades[]){
		Scanner sc = new Scanner(System.in);
		
		for(int i = 0; i < idades.length; i++){
			System.out.print("Digite sua idade: ");
            idades[i] = sc.nextInt();
		}
		for (int i = 0; i<idades.length; i++){
		    System.out.println("Idades --->"+ idades[i]);
	    }
		
	sc.close();   
	return idades;	
	}
	
	public static int maiorNum(int idades[]){
	int maior = idades[0];	
	for (int i = 0; i<idades.length; i++){
	        if (idades[i] > maior){
				maior = idades[i];
			}	
		}	
	return maior;	
	}

}


public class Num{
	
	public static void main(String args[]){
	   int idades[] = {0,0,0,0};
	   Auxiliar.lerVetor(idades);
	
	int maior = Auxiliar.maiorNum(idades);
        System.out.println("Maior idade: " + maior);
	
	}
	
}

==================================================================================================================================
import java.util.Scanner;

class Auxiliar{
	
	public static int maiorVetor(int num[], String nome[]){
		Scanner sc = new Scanner(System.in);
		
		int maior = num[0];
		String nomeM = nome[0];
		
		for(int i = 0; i < num.length &&  i < nome.length; i++){
			
			System.out.print("Diga um nome: ");
            nome[i] = sc.next();
			
			System.out.print("Digite a idade: ");
            num[i] = sc.nextInt();
		}
		for (int i = 0; i<num.length; i++){
		    if (maior< num[i]){
				maior = num[i];
				nomeM = nome[i];
			}
		
	    }
	System.out.println("A pessoa mais velha é " + nomeM + " com " + maior+ " anos!!");
	sc.close();   	
	}
	
}

public class Num{
	
	public static void main(String args[]){
	   int num[] = {0,0,0,0,0};
	   String nomes[] = {"","","","",""};
	   
	Auxiliar.maiorVetor(num,nomes);
	}
	
=====================================================================================================================
import java.util.Scanner;
class Auxiliar {
    public static void Pedir_Idades(int[] idades) {
        Scanner src = new Scanner(System.in);
        for (int i = 0; i < idades.length; i++) {
            System.out.println("Digite uma idade: ");
            idades[i] = src.nextInt();
        }
    }

    public static void Pedir_Nomes(String[] nomes) {
        Scanner src = new Scanner(System.in);
        for (int i = 0; i < nomes.length; i++) {
            System.out.println("Digite um nome: ");
            nomes[i] = src.nextLine();
        }
    }

    public static void Maior_Idades(int[] idades, String[] nomes){
        int maior = idades[0];
        String maiorNome = nomes[0];
        for (int idx = 1; idx < idades.length; idx++) {
            if (idades[idx] > maior) {
                maiorNome = nomes[idx];
                maior = idades[idx];
            }
        }
        System.out.println("A pessoa mais velha é " + maiorNome + " com " + maior + " anos.");
    }
}


public class Vetor3 {
    public static void main(String[] args) {
        int vetor[] = new int[5];
        String vetor2[] = new String[5];
        Auxiliar.Pedir_Idades(vetor);
        Auxiliar.Pedir_Nomes(vetor2);
        Auxiliar.Maior_Idades(vetor, vetor2);
        
    }
}

}
=====================================================================================
import java.util.Scanner;

class Auxiliar{
	
	public static int maiorVetor(int num[], String nome[]){
		Scanner sc = new Scanner(System.in);
		
		int maior = num[0];
		String nomeM = nome[0];
		
		for(int i = 0; i < num.length &&  i < nome.length; i++){
			
			System.out.print("Diga um nome: ");
            nome[i] = sc.next();
			
			System.out.print("Digite a idade: ");
            num[i] = sc.nextInt();
		}
		for (int i = 0; i<num.length; i++){
		    if (maior< num[i]){
				maior = num[i];
				nomeM = nome[i];
			}
		
	    }
	System.out.println("A pessoa mais velha é " + nomeM + " com " + maior+ " anos!!");
	sc.close();   	
	}
	
}

public class Num{
	
	public static void main(String args[]){
	   int num[] = {0,0,0,0,0};
	   String nomes[] = {"","","","",""};
	
    	
	Auxiliar.maiorVetor(num,nomes);
	}
	
}

