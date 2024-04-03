# Delivary-charges
import java.util.Scanner;

public class UserInterface {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Getting input from the user
        System.out.print("Enter the distance (in km): ");
        double distance = scanner.nextDouble();
        
        // Creating CustomerDetails object
        CustomerDetails customer = new CustomerDetails();
        
        // Calculating and displaying bonus points
        double bonusPoints = customer.calculateBonusPoints();
        System.out.println("Bonus Points: " + bonusPoints);
        
        // Calculating and displaying delivery charges
        double deliveryCharges = customer.deliveryCharge(distance);
        System.out.println("Delivery Charges: Rs " + deliveryCharges);
        
        scanner.close();
    }
}

class CustomerDetails {
    // Assuming other relevant attributes and methods exist
    
    public double calculateBonusPoints() {
        // Calculation logic for bonus points
        // Assuming this method exists and returns bonus points
        return 100.0; // Example value
    }
    
    public double deliveryCharge(double distance) {
        double deliveryCharges;
        if (distance >= 25) {
            deliveryCharges = distance * 8;
        } else if (distance >= 15) {
            deliveryCharges = distance * 5;
        } else {
            deliveryCharges = distance * 2;
        }
        return deliveryCharges;
    }
}
