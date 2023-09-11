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

We can also solve it using single traversal but we will have make it two step process. In this first step, we will be checking if the traversing element is smaller than   small variable  element and if found true then we will make the travesing element "smallest" and the small variablem element as second smallest. Further in order to add another level of filtration, we will be making a comparison between traversing element with the second smallest element as well as the traversing element should not be equal to the small variable element then we can update the second smallest variable element to the current traversing element. 


```
package Array;

import java.util.Arrays;

public class Shiva {

    public static void max(int[] arr){
        int max=Integer.MIN_VALUE;
        int min=Integer.MAX_VALUE;
        int second_Max=Integer.MIN_VALUE;
        int second_Min=Integer.MAX_VALUE;
        for(int i=0;i<arr.length;i++){
            if(arr[i]<min ){
                second_Min=min;
                min=arr[i];
            } else if (arr[i]< second_Min && arr[i]!=min ) {
                second_Min=arr[i];
            }
        }
        System.out.println(" second_min "+second_Min);

        for(int i=0;i<arr.length;i++){
            if(arr[i]>max ){
                second_Max=max;
                max=arr[i];
            } else if (arr[i]> second_Max && arr[i]!=max) {
                second_Max=arr[i];
            }
        }
        System.out.println(" second_max "+ second_Max);
    }


    public static void main(String[] args) {
        int[] arr={2,21,0,2,1,3,2};
max(arr);

    }
}

```
