# Difference-Arrays-ArrayLists
This repository dives into the differences between Arrays and ArrayLists in JAVA
package difference_arrays_arraylists;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

public class DifferenceArraysArrayLists {

    public static void main(String[] args) {
        
System.out.println(" Project Name: Difference Arrays-ArrayLists ");
System.out.println();
System.out.println();

        // -------------------- Arrays --------------------
        System.out.println("----- Demonstrating Arrays -----");
        System.out.println();
        System.out.println("// Difference in Arrays 1 - Size: Have a set size and unable to change.//");
        int[] fixedSizeArray = new int[5];
        System.out.println("// Declares an array that can hold 5 integers.//");
        System.out.println("Array 'fixedSizeArray' declared with a fixed size of: " + fixedSizeArray.length);
        System.out.println("// fixedSizeArray[5] = 10; // This would cause an ArrayIndexOutOfBoundsException at runtime, demonstrating the fixed size.//");
        System.out.println();
        System.out.println("// Difference in Arrays 2 - Memory: The computer sets a specific amount of space which stays the same.//");
        System.out.println("Memory for 'fixedSizeArray' is allocated as a contiguous block of size for 5 integers.");
        System.out.println();
        System.out.println("// Difference in Arrays 3 - Tools: No built-in methods for Dynamic Operations: Arrays don't have built-in methods for easy addition, removal, or resizing of elements. These operations typically require manual implementation.//");
        fixedSizeArray[0] = 10;
        fixedSizeArray[1] = 20;
        System.out.println("Elements in 'fixedSizeArray' after adding some values: " + Arrays.toString(fixedSizeArray));
        System.out.println("// To remove or add in the middle of an array, Programmers would typically need to create a new array.//");
        int[] newArrayWithRemoval = new int[fixedSizeArray.length - 1];
        int removeIndex = 0;
        int newArrayIndex = 0;
        for (int i = 0; i < fixedSizeArray.length; i++) {
            if (i != removeIndex) {
                newArrayWithRemoval[newArrayIndex++] = fixedSizeArray[i];
            }
        }
        System.out.println("Manually 'removing' element at index " + removeIndex + ": " + Arrays.toString(newArrayWithRemoval));
        System.out.println();
        System.out.println("// Difference in Arrays 4 - Keeping the Same Type: Java uses an enforcing mechanism for all elements within a single array must be the same data type establishing time stamp of array's declaration and creation.//");
        System.out.println("// fixedSizeArray[2] = 'hello' // This would cause a compile-time error as the array is of type int.//");
        System.out.println("Array 'fixedSizeArray' is of type int, so it can only hold integer values.");
        System.out.println();
        System.out.println("// Difference in Array 5 - Basic Types: Can directly hold simple items like numbers, true / false, usage of booleans values.//");
        boolean[] booleanArray = {true, false, true};
        System.out.println("Array 'booleanArray' holding primitive boolean values: " + Arrays.toString(booleanArray));

        System.out.println("\n----- Demonstrating ArrayLists -----");
        System.out.println();
        // -------------------- ArrayLists --------------------

        System.out.println("// Difference in ArrayLists 1 - Size: Can enlarge and shrink as programmers add or remove items within elements.//");
        ArrayList<Integer> dynamicSizeList = new ArrayList<>(); // Creates an empty ArrayList.
        System.out.println("ArrayList 'dynamicSizeList' initial size: " + dynamicSizeList.size());
        dynamicSizeList.add(100);
        dynamicSizeList.add(200);
        System.out.println("ArrayList 'dynamicSizeList' size after adding elements: " + dynamicSizeList.size());
        dynamicSizeList.remove(0);
        System.out.println("ArrayList 'dynamicSizeList' size after removing an element: " + dynamicSizeList.size());
        System.out.println();
        System.out.println("// Difference in ArrayLists 2 - Memory: The computer can get more space if needed which can be complicated.//");
        System.out.println("ArrayList 'dynamicSizeList' can dynamically resize its underlying array in memory as needed.");
        System.out.println();
        System.out.println("// Difference in ArrayLists 3 - Tools: Provides programmers more flexibility of adding, removing, searching and resizing items, rearrange and find items using various built-in tool methods.//");
        dynamicSizeList.add(0, 50); System.out.println("// Adds 50 at index 0 //");
        System.out.println("ArrayList 'dynamicSizeList' after adding at a specific index: " + dynamicSizeList);
        dynamicSizeList.remove(Integer.valueOf(200)); // Removes the first occurrence of the value 200
        System.out.println("ArrayList 'dynamicSizeList' after removing a specific value: " + dynamicSizeList);
        boolean contains50 = dynamicSizeList.contains(50);
        System.out.println("ArrayList 'dynamicSizeList' contains 50: " + contains50);
        System.out.println();
        System.out.println("// Difference in ArrayLists 4 - Keeping the Same Type: Uses a feature calle \"generics\" to help ensure programmers input error-free items of elements by catching mistakes early.//");
        System.out.println("// dynamicSizeList.add 'hello'.  This would cause a compile-time error because the ArrayList is of type Integer due to generics.//");
        ArrayList<String> stringList = new ArrayList<>();
        stringList.add("apple");
        stringList.add("banana");
        System.out.println("ArrayList 'stringList' holding String objects (due to generics): " + stringList);
        System.out.println();
        System.out.println("// Difference in ArrayLists 5 - Basic Types: Holds more complex \"object,\" which executed automatically.//");
        System.out.println("// ArrayLists hold objects. For primitive types, they use their wrapper classes (e.g., Integer for int, Boolean for boolean) through autoboxing.//");
        ArrayList<Boolean> booleanList = new ArrayList<>();
        booleanList.add(true); System.out.println("// Autoboxing: boolean to Boolean//");
        booleanList.add(false);
        System.out.println("ArrayList 'booleanList' holding Boolean objects (wrapper for boolean): " + booleanList);
    }
}
