package modulo1;

import java.util.Scanner;

public class CupomFiscal {

    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        // Exibe o cabeçalho do cupom
        imprimirCabecalho();

        // Cadastro dos produtos (simples para simulação)
        System.out.print("Digite o nome do produto: ");
        String produto1 = entrada.nextLine();

        System.out.print("Digite a quantidade: ");
        int qtd1 = entrada.nextInt();

        System.out.print("Digite o preço unitário: ");
        double preco1 = entrada.nextDouble();

        // Exemplo de um segundo produto
        entrada.nextLine(); // consumir quebra de linha
        System.out.print("Digite o nome do segundo produto: ");
        String produto2 = entrada.nextLine();

        System.out.print("Digite a quantidade: ");
        int qtd2 = entrada.nextInt();

        System.out.print("Digite o preço unitário: ");
        double preco2 = entrada.nextDouble();

        // Exibe os produtos
        imprimirProdutos(produto1, qtd1, preco1, produto2, qtd2, preco2);

        // Calcula e exibe o total
        double total = (qtd1 * preco1) + (qtd2 * preco2);
        imprimirTotal(total);

        // Exibe mensagem de agradecimento
        imprimirMensagemFinal();

        entrada.close();
    }

    // Método para exibir o cabeçalho da loja
    public static void imprimirCabecalho() {
        System.out.println("===================================");
        System.out.println("      SUPERMERCADO BOM PREÇO");
        System.out.println("       CNPJ: 12.345.678/0001-99");
        System.out.println("     Rua Principal, nº 123 - Centro");
        System.out.println("===================================");
    }

    // Método para exibir a lista de produtos
    public static void imprimirProdutos(String p1, int q1, double v1, String p2, int q2, double v2) {
        System.out.println("\nPRODUTOS:");
        System.out.printf("%-20s %5d x R$ %.2f = R$ %.2f\n", p1, q1, v1, (q1 * v1));
        System.out.printf("%-20s %5d x R$ %.2f = R$ %.2f\n", p2, q2, v2, (q2 * v2));
    }

    // Método para exibir o valor total
    public static void imprimirTotal(double total) {
        System.out.println("-----------------------------------");
        System.out.printf("TOTAL A PAGAR: R$ %.2f\n", total);
        System.out.println("-----------------------------------");
    }

    // Método para exibir a mensagem final
    public static void imprimirMensagemFinal() {
        System.out.println("Obrigado pela preferência!");
        System.out.println("Volte sempre :)");
    }
}
