import java.util.Scanner;

public class CalculadoraPrecoVenda {

    public static void main(String[] args) {
    
        Scanner scanner = new Scanner(System.in);

        System.out.print("Digite o preço de custo do produto: ");
        
        double precoCusto = scanner.nextDouble();

        double precoVenda = calcularPrecoVenda(precoCusto);

        System.out.println("O preço de venda do produto é: R$" + precoVenda);

        scanner.close();
    }

    public static double calcularPrecoVenda(double precoCusto) {
    
        double lucro;
        
        if (precoCusto < 10.0) {
        
            lucro = 0.7; // 70%
            
        } else if (precoCusto < 30.0) {
        
            lucro = 0.5; // 50%
            
        } else if (precoCusto < 50.0) {
        
            lucro = 0.4; // 40%
            
        } else {
        
            lucro = 0.3; // 30%
            
        }

        return precoCusto * (1 + lucro);
        
    }
    
}
