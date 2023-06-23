# Assignment_2-Removal_Element-

import java.util.Scanner;

public class Main{

    static int removeElement(int[] arr, int nums){

        int n = arr.length;
        int k = 0; // number of elements not equal to val
        int  val = 0;
        for (int i = 0; i < n; i++) {
            if (arr[i] != val) {
                arr[k] = arr[i];
                k++;
            }
        }

        return k;



    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the array size");
        int n = sc.nextInt();
        int[] arr = new int[n];

        System.out.println("Enter " + n + " elements");
        for(int i = 0; i < n; i++){
            arr[i] = sc.nextInt();
        }

        System.out.println("Enter the value ");
        int nums = sc.nextInt();
        System.out.println(removeElement(arr, nums));
    }

}
