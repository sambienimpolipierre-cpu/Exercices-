import java.util.Scanner;

public class Factoriel {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Entrez un nombre entier positif :");
        int nombre = scanner.nextInt();
        scanner.close();

        if (nombre < 0) {
            System.out.println("Le factoriel n'est pas défini pour les nombres négatifs.");
        } else {
            long factoriel = calculerFactoriel(nombre);
            System.out.println("Le factoriel de " + nombre + " est : " + factoriel);
        }
    }

    public static long calculerFactoriel(int n) {
        if (n == 0 || n == 1) {
            return 1;
        } else {
            return n * calculerFactoriel(n - 1);
        }
    }
}
