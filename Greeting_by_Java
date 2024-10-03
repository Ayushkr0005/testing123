import java.time.LocalTime;
import java.time.format.DateTimeFormatter;
import java.util.Scanner;

public class GreetingBasedOnUserTime {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        LocalTime morningStart = LocalTime.of(5, 0); 
        LocalTime afternoonStart = LocalTime.of(12, 0);
        LocalTime eveningStart = LocalTime.of(17, 0);   
        LocalTime nightStart = LocalTime.of(21, 0);    

        System.out.print("Enter the time in HH:MM format (24-hour): ");
        String userInput = scanner.nextLine();
        

        LocalTime userTime;
        try {
            userTime = LocalTime.parse(userInput, DateTimeFormatter.ofPattern("HH:mm"));
        } catch (Exception e) {
            System.out.println("Invalid time format. Please use HH:MM format.");
            return;
        }


        if (userTime.isAfter(morningStart) && userTime.isBefore(afternoonStart)) {
            System.out.println("Good Morning");
        } else if (userTime.isAfter(afternoonStart) && userTime.isBefore(eveningStart)) {
            System.out.println("Good Afternoon");
        } else if (userTime.isAfter(eveningStart) && userTime.isBefore(nightStart)) {
            System.out.println("Good Evening");
        } else {
            System.out.println("Good Night");
        }

        DateTimeFormatter formatter = DateTimeFormatter.ofPattern("hh:mm a");
        System.out.println("Entered Time: " + userTime.format(formatter));
        
        scanner.close();
    }
}
