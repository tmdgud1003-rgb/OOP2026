# OOP2026
### Homework1
```java
package homework;

public class homework {
	public static void main(String []args){
		int n = 10;
        System.out.println("");
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("#");
            }
            System.out.println("");
        }

        for (int i = n; i >= 1; i--) {
            for (int j = 1; j <= i; j++) {
                System.out.print("#");
            }
            System.out.println("");
        }

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n - i; j++) {
                System.out.print(" ");
            }
            for (int k = 1; k <= i; k++) {
                System.out.print("#");
            }
            System.out.println("");
        }

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j < i; j++) {
                System.out.print(" ");
            }
            for (int k = 1; k <= n - i + 1; k++) {
                System.out.print("#");
            }
            System.out.println();
        }
    }
}
```
### Homework2
```java
package homework1;

public class homework1 {
	public static void main(String []args){
		int rows = 7;
        int[][] binomial = new int[rows][];

        for (int n = 0; n < rows; n++) {
            binomial[n] = new int[n + 1];
            binomial[n][0] = 1;
            binomial[n][n] = 1;

            for (int k = 1; k < n; k++) {
                binomial[n][k] = binomial[n - 1][k - 1] + binomial[n - 1][k];
            }
        }

        System.out.println(" 이항계수 ");
        for (int n = 0; n < rows; n++) {
            for (int k = 0; k <= n; k++) {
                System.out.print(binomial[n][k] + " ");
            }
            System.out.println();
        }
    }
}
```
<img width="886" height="476" alt="스크린샷 2026-09-15 142431" src="https://github.com/user-attachments/assets/5f6334c7-e1ef-4636-8fa0-87cc49a9ed2d" />
