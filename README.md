import java.util.Scanner;

public class WordCounter {
    public static void main(String[] args) {
        // Utwórz obiekt Scanner do wczytywania danych od użytkownika
        Scanner scanner = new Scanner(System.in);

        // Poproś użytkownika o wpisanie ciągu znaków
        System.out.print("Wprowadź ciąg znaków: ");
        String input = scanner.nextLine();

        // Usuń dodatkowe spacje z początku i końca ciągu
        input = input.trim();

        // Sprawdź, czy ciąg nie jest pusty
        if (input.isEmpty()) {
            System.out.println("Liczba słów: 0");
        } else {
            // Podziel ciąg po jednej lub większej liczbie spacji
            String[] words = input.split("\\s+");
            System.out.println("Liczba słów: " + words.length);
        }

        scanner.close();
    }
}
