
Herein, the first loop is reponsible for the rows whatever changes we have got to make in the rows we do it in the first for loop. 
Second for loop is for the columns.

###  Box
Check here, we are just changing the row in the first for loop using new line and in the second loop we are just printing the * without changing the line. 
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
       
 draw(5);

    }
}

*****
*****
*****
*****
*****
```
### Half Triangle (Opposite)
```
package Array;

import java.util.Arrays;

public class Shiva {

    public static void draw(int n){
        for(int i=0;i<n;i++){
            System.out.println("");
            for(int j=i;j<n;j++){
                System.out.print("*");
            }
        }
    }


    public static void main(String[] args) {
        
 draw(5);

    }
}
*****
****
***
**
*
```
### Half Triangle 
```
package Array;

import java.util.Arrays;

public class Shiva {

    public static void draw(int n){
        for(int i=0;i<n;i++){
            System.out.println("");
            for(int j=i;j>=0;j--){
                System.out.print("*");
            }
        }
    }


    public static void main(String[] args) {

     draw(5);

    }
}

*
**
***
****
*****
```

### Half Triangle with Number (Opposite)

```
package Array;

import java.util.Arrays;

public class Shiva {

    public static void draw(int n){
        for(int i=1;i<=n;i++){
            System.out.println("");
            for(int j=i;j<=n;j++){
                System.out.print(j);
            }
        }
    }


    public static void main(String[] args) {

 draw(5);

    }
}
```

### Half Triangle with Number

Herein, observe that for printing the number. First for loop will be creating row and the second loop should be running upto the number of time first loop is running or  we run the outer loop for N times as we have to print N rows, and since we have to print a right-angled triangle/pyramid which must be upright, so the inner loop will run for the row number in each iteration.

```
package Array;

import java.util.Arrays;

public class Shiva {

    public static void draw(int n){
        for(int i=1;i<=n;i++){
            System.out.println("");
            for(int j=1;j<=i;j++){
                System.out.print(j);
            }
        }
    }


    public static void main(String[] args) {

 draw(5);

    }
}

1
12
123
1234
12345
```





