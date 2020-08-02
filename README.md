# Linear Search

A simple single class implementation of linear search in Java. The user will be prompted to input the number of elements in a list which they want to enter. The user then will choose an element to be searched in the list. The linear search algorithm will be automatically performed, and the index at which the target was found will be returned or the code will notify that it could not find the target. In either case, the created list will be returned as well.

## How to use it.
* Open a command prompt window and go to the directory where you saved the java program (LinearSearch.java).
* Type 'javac LinearSearch.java' and press enter to compile your code. If there are no errors in your code, the command prompt will take you to the next line.
* Now, type 'java LinearSearch' to run your program.
* You will be able to see an output line and asking input to enter the number of elements you want to enter.
* Next you will enter the number of elements it can be space-separated or in a new line.
* After completion of entering elements in the list, the program will be asking for the element which you want to search.
* And finally you see the result in which index given element is available in the list. in case of an unavailable element, error message will be printed on the screen.

## Code
```
import java.util.Scanner;

/**
 * This is an implementation of the linear search algorithm.
 * @author @inforkgodara
 *
 */
public class LinearSearch {

    /**
     * Linear search implementation.
     * @param list the array to be searched.
     * @param search the element being looked for in the array.
     * @return the index at which the search element was first found or -1 if not found.
     */
    public static int search(int[] list, int search) {
        int length = list.length;
        for (int index = 0; index < length; index++) {
            if (list[index] == search) {
                return index;
            }
        }
        return -1;
    }

    public static void main(String[] args) {
        System.out.print("Enter length of list : ");
        Scanner scanner = new Scanner(System.in);

        int length = scanner.nextInt();
        int[] list = new int[length];

        for (int index = 0; index < length; index++) {
            list[index] = scanner.nextInt();
        }

        System.out.print("Enter element to search : ");
        int search = scanner.nextInt();
        int elementAt = search(list, search);

        String result = elementAt == -1 ? "Element not found." : "Element is at index " + elementAt;
        System.out.println(result);
    }
}
```