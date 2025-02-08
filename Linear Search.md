````java []
import java.util.Scanner;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int a[] = {100,200,300,400,500};
        System.out.println("Enter your Element:");
        int key = sc.nextInt();
        
        int start = 0;
        int end = a.length-1;
        int flag=0;
        while(start<=end){
            int mid =(start+end)/2;
            if(a[mid]==key){
                System.out.println("Element Found:" + mid);
                flag=1;
                break;
            }
            else if(a[mid]<key){
                start = mid+1;
            }
            else {
                end = mid-1;
            }
        }
        if(flag==0){
        System.out.println("Element not found");
    }
    }
}
````



# output
````java []
Enter your Element:
200
Element Found:1

````

