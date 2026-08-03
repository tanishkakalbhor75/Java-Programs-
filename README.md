import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number (0-1000): ");
        int num = sc.nextInt();

        int temp = num;
        int sum = 0;

        while (temp > 0) {
            sum += temp % 10;
            temp = temp / 10;
        }

        int original = sum;
        int reverse = 0;

        while (original > 0) {
            reverse = reverse * 10 + (original % 10);
            original = original / 10;
        }

        System.out.println("Digit Sum = " + sum);

        if (sum == reverse) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not a Palindrome");
        }

        sc.close();
    }
}
