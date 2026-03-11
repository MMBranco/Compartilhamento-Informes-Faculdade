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
