```` java[]
import java.util.Arrays;

public class InsertionSort {
    public static void main(String[] args) {
        int[] arr = {2, -6, -3, 8, -23, 76, 86, 23, 3};
        Insertion(arr);
        System.out.println(Arrays.toString(arr));

    }

    static void Insertion(int[] arr) {
        for (int i = 0; i < arr.length - 1; i++) {
            for (int j = i + 1; j > 0; j--) {
                if (arr[j] < arr[j - 1]) {
                    swap(arr, j, j - 1);
                } else {
                    break;
                }
            }
        }
    }

    static void swap(int[] arr, int index1, int index2) {
        int temp = arr[index1];
        arr[index1] = arr[index2];
        arr[index2] = temp;
    }
}
````
# Output
```` java[]
[-23, -6, -3, 2, 3, 8, 23, 76, 86]
````
