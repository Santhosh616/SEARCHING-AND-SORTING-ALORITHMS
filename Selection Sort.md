```` java[]
import java.util.Arrays;

public class SelectionSort {
    public static void main(String[] args) {
        int[] arr = {2, -6, -3, 8, -23, 76, 86, 23, 3};
        selecting(arr);
        System.out.println(Arrays.toString(arr));
    }

    static void selecting(int[] arr){
        for (int i = 0; i < arr.length ; i++) {
            int Last = arr.length-i-1;
            int MaxIndex = getMaxIndex(arr,0,Last);
            swap(arr,MaxIndex,Last);
        }

    }

    static int getMaxIndex(int[] arr, int start,int end){       //input index.
        int Max = start;
        for (int i = 0; i <= end ; i++) {
            if(arr[Max] < arr[i]){
                Max = i;
            }
        }
        return Max;
    }

    static void swap(int[] arr, int index1, int index2){        //input index.
        int temp = arr[index1];
        arr[index1] = arr[index2];
        arr[index2] = temp;
    }
}
````
# Output
````
[-23, -6, -3, 2, 3, 8, 23, 76, 86]
````
