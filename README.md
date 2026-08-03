import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number (0-1000): ");
        int num = sc.nextInt();

        int original = num;
        int sum = 0;

        while (num > 0) {
            sum += num % 10;
            num = num / 10;
        }

        String str = String.valueOf(original);
        String encrypted = "";

        for (int i = 0; i < str.length(); i++) {
            int digit = str.charAt(i) - '0';
            digit = (digit + sum) % 10;
            encrypted += digit;
        }

        System.out.println("Digit Sum = " + sum);
        System.out.println("Encrypted Number = " + encrypted);

        sc.close();
    }
}
