# meu_novo_projeto
public class contadobanco {

	
	public double adcsaldo (double saldo,double valor)
	{		
		return (saldo + valor);
	}
	public double remSaldo ( double saldo, double valor)
	{	
		return (saldo - valor);

	}

}

import javax.swing.JOptionPane;

import java.util.Scanner;

public class Contacorrente {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc= new Scanner(System.in);
		
		System.out.println("Digite o seu nome: ");
		String nome = sc.next();
		System.out.println("Digite sua agência: ");
		int agencia = sc.nextInt();
		System.out.println("Digite o número de sua conta: ");
		int contacorrente = sc.nextInt();
		
		double saldo = 0;
		 
		System.out.println("Digite qual operação deseja realizar: (0-Adicionar ou 1-Remover)");
		int operacao = sc.nextInt();
		contadobanco um = new contadobanco();
		 
		
		if (operacao == 0 ) {
			System.out.println("Digite o valor que deseja Adicionar: ");
			double valor1 = sc.nextDouble();
			double saldo2 = um.adcsaldo (saldo,valor1);
	
			System.out.println("Seu saldo total dísponivel é: R$" + saldo2);
			
		}
		
		if(operacao == 1 ) {
			System.out.println("Digite o valor que deseja Remover: ");
			double valor1 = sc.nextDouble();
			double saldo2 = um.remSaldo (saldo, valor1);
			
			System.out.println("Seu saldo total dísponivel é: R$" + saldo2);
			
		}
		
		
		
	}

}
