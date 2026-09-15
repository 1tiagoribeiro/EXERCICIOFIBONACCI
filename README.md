import java.util.Scanner;

public class Fibonacci {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        System.out.print("Digite a quantidade de termos (N): ");
        int n = entrada.nextInt();

        long primeiro = 0;
        long segundo = 1;

        System.out.println("Sequência de Fibonacci:");

        for (int i = 0; i < n; i++) {
            System.out.print(primeiro);

            if (i < n - 1) {
                System.out.print(", ");
            }

            long proximo = primeiro + segundo;
            primeiro = segundo;
            segundo = proximo;
        }

        entrada.close();
    }
}
