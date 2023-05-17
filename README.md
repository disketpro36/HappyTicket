# HappyTicket
HappyTicket
import java.util.Scanner;

public class HappyTicket {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Введите номер билета: ");
        int ticketNumber = scanner.nextInt();

        boolean isHappyTicket = checkHappyTicket(ticketNumber);
        if (isHappyTicket) {
            System.out.println("Билет является счастливым!");
        } else {
            System.out.println("Билет не является счастливым.");
        }
    }

    public static boolean checkHappyTicket(int ticketNumber) {
        int sumFirstHalf = 0;
        int sumSecondHalf = 0;

        String ticketString = String.valueOf(ticketNumber);
        int length = ticketString.length();
        for (int i = 0; i < length / 2; i++) {
            sumFirstHalf += Character.getNumericValue(ticketString.charAt(i));
            sumSecondHalf += Character.getNumericValue(ticketString.charAt(length - i - 1));
        }

        return sumFirstHalf == sumSecondHalf;
    }
}
