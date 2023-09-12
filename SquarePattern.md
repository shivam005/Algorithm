
Herein, the first loop is reponsible for the rows whatever changes we have got to make in the rows we do it in the first for loop. 
Second for loop is for the columns.

```
package Array;

import java.util.Arrays;

public class Shiva {

    public static void draw(int n){
        for(int i=0;i<n;i++){
            System.out.println("");
            for(int j=0;j<n;j++){
                System.out.print("*");
            }
        }
    }


    public static void main(String[] args) {
        int[] arr={2,21,0,2,1,3,2};
 draw(5);

    }
}

```
