# Interface-Example
#Program:
import java.util.Scanner;
// Interface with two methods
interface UserDetails {
 String getUserValue();
 void displayUserDetail(String userDetails);
}
// Class implementing the interface
class User implements UserDetails {
 private String name, address;
 private int age;
 // Overriding getUserValue method
 public String getUserValue() {
 Scanner scanner = new Scanner(System.in);

 System.out.print("Enter your name: ");
 name = scanner.nextLine();

 System.out.print("Enter your address: ");
 address = scanner.nextLine();

 System.out.print("Enter your age: ");
 age = scanner.nextInt();

 return "Name: " + name + "\nAddress: " + address + "\nAge: " + age;
 }
 // Overriding displayUserDetail method
 public void displayUserDetail(String userDetails) {
 System.out.println("User Details:\n" + userDetails);
 }
}
public class Main {
 public static void main(String[] args) {
 User user = new User();
 String details = user.getUserValue(); // Getting user details
 user.displayUserDetail(details); // Displaying user details
 }
}
