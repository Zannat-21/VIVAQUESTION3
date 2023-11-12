# VIVAQUESTION3
```
/*
3. Create a program that converts a binary number to its decimal equivalent.
Prompt the user to input a binary number, and then convert and display its
decimal equivalent.
*/
package BinaryToDecimal;
import java.util.Scanner;
public class BinaryToDecimal{
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a binary number: ");
        String binaryNumber = scanner.nextLine();

        // Check if the input is a valid binary number
        if (isBinary(binaryNumber)) {
            int decimalNumber = Integer.parseInt(binaryNumber, 2);/*This line converts the valid binary number (stored as a string) to 
                                                                  its decimal equivalent using the Integer.parseInt method with a radix or base of 2. */
                                                                  
            System.out.println("The decimal equivalent of " + binaryNumber + " is: " + decimalNumber);
        } else {
            System.out.println("Invalid input. Please enter a valid binary number (consisting of 0s and 1s).");
        }
    }  
/*The 'isBinary' function is a function that uses regular expressions to check if the input consists of only 0s and 1s. 
If an invalid digit is found, it returns false, and the program displays an error message and exits. 
If the input is valid, the program proceeds to convert the binary number to decimal.
*/

    // Function to check if a string is a valid binary number
    public static boolean isBinary(String input) { 
          for (char c : input.toCharArray()) { //for (each) loop was used
   
             if (c != '0' && c != '1') {           
                return false;
           }
        }
        return true;
    }

}
```
