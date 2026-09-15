# OOP2026
### Homework
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

### Homework2
int rows = 7; // 0행부터 6행까지 (총 7행)
        int[][] binomial = new int[rows][];

        for (int n = 0; n < rows; n++) {
            binomial[n] = new int[n + 1];
            binomial[n][0] = 1;     // 맨 앞은 1
            binomial[n][n] = 1;     // 맨 끝은 1

            for (int k = 1; k < n; k++) {
                binomial[n][k] = binomial[n - 1][k - 1] + binomial[n - 1][k];
            }
        }

        // 결과 출력
        System.out.println("=== 파스칼의 삼각형 (이항계수) ===");
        for (int n = 0; n < rows; n++) {
            for (int k = 0; k <= n; k++) {
                System.out.print(binomial[n][k] + " ");
            }
            System.out.println();
        }
    }
}
