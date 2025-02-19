# linked-list-and-array-list
import java.util.ArrayList;
import java.util.LinkedList;
import java.util.List;
import java.util.Scanner;
public class SimpleUserInputListManipulation {
public static void main(String[] args) {
 LinkedList<Integer> linkedList = new LinkedList<>();
ArrayList<Integer> arrayList = new ArrayList<>();
List<Integer> commonList;
Scanner scanner = new Scanner(System.in);
System.out.print("Enter integers separated by spaces: ");
String input = scanner.nextLine();
String[] elements = input.split("\\s+");
for (String element : elements) {
int number = Integer.parseInt(element);
linkedList.add(number);
arrayList.add(number);
}
System.out.println("Initial Linked List: " + linkedList);
System.out.println("Initial Array List: " + arrayList);
System.out.print("Enter elements to be added (separated by spaces): ");
String elementsToAddInput = scanner.nextLine();
String[] elementsToAdd = elementsToAddInput.split("\\s+");
linkedList.addFirst(Integer.parseInt(elementsToAdd[0]));
arrayList.add(0, Integer.parseInt(elementsToAdd[0]));
linkedList.addLast(Integer.parseInt(elementsToAdd[1]));
arrayList.add(Integer.parseInt(elementsToAdd[1]));
    System.out.println("Final Linked List:"+linkedList);
    System.out.println("Final Array List:");
    scanner.close();
}
}
OUTPUT:
Enter integers separated by spaces: 10 20 30 40
Initial Linked List: [10, 20, 30, 40]
Initial Array List: [10, 20, 30, 40]
Enter elements to be added (separated by spaces): 5 50
Final Linked List: [5, 10, 20, 30, 40, 50]
Final Array List: [5, 10, 20, 30, 40, 50]
