# Exercises-using-collection-framework-Linked-List-and-Array-List
package simpleuserinputlistmanipulation;

import java.util.ArrayList;
import java.util.LinkedList;
import java.util.List;
import java.util.Scanner;

/**
 *
 * @author 1BSCCSA31
 */
public class SimpleUserInputListManipulation {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
          LinkedList<Integer> linkedList = new LinkedList<>();
        ArrayList<Integer> arrayList = new ArrayList<>();
        List<Integer> commonList;

        // Get the list of integers from the user
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter integers separated by spaces: ");
        String input = scanner.nextLine();

        // Parse the input string and add elements to both lists
        String[] elements = input.split("\\s+");
        for (String element : elements) {
            int number = Integer.parseInt(element);
            linkedList.add(number);
            arrayList.add(number);
        }

        // Display initial lists
        System.out.println("Initial Linked List: " + linkedList);
        System.out.println("Initial Array List: " + arrayList);

        // Get elements to be added from the user
        System.out.print("Enter elements to be added (separated by spaces): ");
        String elementsToAddInput = scanner.nextLine();
        String[] elementsToAdd = elementsToAddInput.split("\\s+");

        // Add elements at the beginning and end of both lists
        linkedList.addFirst(Integer.parseInt(elementsToAdd[0]));
        arrayList.add(0, Integer.parseInt(elementsToAdd[0]));

        linkedList.addLast(Integer.parseInt(elementsToAdd[1]));
        arrayList.add(Integer.parseInt(elementsToAdd[1]));

        // Display the final lists
        System.out.println("Final Linked List: " + linkedList);
        System.out.println("Final Array List: " + arrayList);

        // Close the scanner to avoid resource leaks
        scanner.close();

    }
    
}

Output:
Enter integers separated by spaces: 31 20 19
Initial Linked List: [31, 20, 19]
Initial Array List: [31, 20, 19]
Enter elements to be added (separated by spaces): 16 17
Final Linked List: [16, 31, 20, 19, 17]
Final Array List: [16, 31, 20, 19, 17]
