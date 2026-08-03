import java.util.Scanner;

public class Main {

    // Method to calculate the sum of digits
    public static int digitSum(int num) {
        int sum = 0;
        while (num > 0) {
            sum += num % 10;
            num = num / 10;
        }
        return sum;
    }

    // Method to reverse a number
    public static int reverse(int num) {
        int rev = 0;
        while (num > 0) {
            rev = rev * 10 + (num % 10);
            num = num / 10;
        }
        return rev;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter an integer (0-1000): ");
        int num = sc.nextInt();

        int reversed = reverse(num);
        int targetSum = digitSum(reversed);

        System.out.println("Numbers between 0 and 1000 with digit sum " + targetSum + " are:");

        for (int i = 0; i <= 1000; i++) {
            if (digitSum(i) == targetSum) {
                System.out.print(i + " ");
            }
        }

        sc.close();
    }
}
