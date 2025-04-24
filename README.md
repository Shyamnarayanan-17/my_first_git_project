import java.util.Scanner;

public class LeapYear {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter a year: ");
        int year = scanner.nextInt();
        
        if (isLeapYear(year)) {
            System.out.println(year + " is a leap year.");
        } else {
            System.out.println(year + " is not a leap year.");
        }
        
        scanner.close();
    }
    
    public static boolean isLeapYear(int year) {
        // A year is a leap year if:
        // 1. It's divisible by 400, OR
        // 2. It's divisible by 4 but not by 100
        return (year % 400 == 0) || (year % 100 != 0 && year % 4 == 0);
    }
}
