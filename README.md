# Lca-2-java
Employee Experience Calculator (java.time package)
import java.time.LocalDate;
import java.time.Period;
import java.time.format.DateTimeFormatter;
import java.util.Scanner;

public class lca {
	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		System.out.print("Enter employee name: ");
		String name = scanner.nextLine();
		System.out.print("Enter joining date (yyyy-MM-dd): ");
		LocalDate joiningDate = LocalDate.parse(scanner.nextLine());
		Period experience = Period.between(joiningDate, LocalDate.now());

		System.out.println("\nEmployee Name: " + name);
		System.out.println("Joining Date: "
				+ joiningDate.format(DateTimeFormatter.ofPattern("dd-MMM-yyyy")));
		System.out.println("Experience: " + experience.getYears() + " years, "
				+ experience.getMonths() + " months, " + experience.getDays() + " days");
		scanner.close();
	}
}
