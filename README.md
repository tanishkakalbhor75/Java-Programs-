import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter an integer: ");
        int num = sc.nextInt();

        num = Math.abs(num); // Handles negative numbers
        int largest = 0;

        if (num == 0) {
            largest = 0;
        } else {
            while (num != 0) {
                int digit = num % 10;
                if (digit > largest) {
                    largest = digit;
                }
                num = num / 10;
            }
        }

        System.out.println("Largest digit = " + largest);

        sc.close();
    }
}
