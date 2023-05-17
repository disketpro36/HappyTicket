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
