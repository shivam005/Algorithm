### Find Second Smallest and Second Largest Element in an array

Here in, we will first try to find out the maximum and minimum value using a loop wherein we will be traversing and making comparison with the min or max variable which will be initialized by some value. Further in order to find the second max or min value, we will be using same approach but this time, we will exclude the previously calculated max and min value. This way, we will have second smallest and largest value. Make sure to have freshly created second min or max variable while making comparison with the array or else you will be ending up with the incorrect ans as it will be trying to be find the maximum and minimum value based on the previously calculated and stored max or min value. 

```
package Array;

import java.util.Arrays;

public class Shiva {

    public static void max(int[] arr){
        int min=arr[0];
        int max=arr[0];
        int second_Min=arr[0];
        int second_Max=arr[0];

        for(int i=0;i< arr.length;i++){
            min=Integer.min(arr[i],min);
            max=Integer.max(arr[i], max);
        }
        System.out.println("min = "+min+" max = "+max);
        for(int i=0;i<arr.length;i++){
            if(arr[i]<second_Min && arr[i]!=min){
                second_Min=arr[i];
            } else if (arr[i]>second_Max && arr[i]!=max) {
                second_Max=arr[i];
            }
        }
        System.out.println("second_max "+ second_Max+ " second_min "+second_Min);
    }


    public static void main(String[] args) {
        int[] arr={2,21,0,2,1,3,2};
max(arr);

    }
}

```
