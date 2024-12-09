# SelectionSort
selection sort implementation in java

import java.util.Arrays;

public class SelectionSort {
    //  perform selection sort
    public static void selectionSort(int[] array) {
        int n = array.length;

        for (int i = 0; i < n - 1; i++) {
            // index of the smallest element in the unsorted part
            int minIndex = i;
            for (int j = i + 1; j < n; j++) {
                if (array[j] < array[minIndex]) {
                    minIndex = j;
                }
            }

            // Swap the smallest element with the first unsorted element
            int temp = array[minIndex];
            array[minIndex] = array[i];
            array[i] = temp;

            // Print the array after each pass (optional)
            System.out.println("Pass " + (i + 1) + ": " + Arrays.toString(array));
        }
    }

    // Main method to test the algorithm
    public static void main(String[] args) {
        int[] array = {64, 25, 12, 22, 11};
        System.out.println("Original Array: " + Arrays.toString(array));

        selectionSort(array);

        System.out.println("Sorted Array: " + Arrays.toString(array));
    }
}

