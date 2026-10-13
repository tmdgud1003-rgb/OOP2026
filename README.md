
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
### Homework4
```java
package homework1;

public class homework1 {
	public static void main(String[] args) {
		for (int j = 1; j <= 9; j++) {
            for (int i = 1; i <= 9; i++) {
                System.out.printf("%d*%d=%-2d  ", i, j, (i * j));
            }
            System.out.println();
        }
    }
}
```
<img width="1720" height="815" alt="구구단출력" src="https://github.com/user-attachments/assets/4c2cec7b-a0ca-4c5a-8e53-6a4e3bead1d7" />

### Homework5
```java
package homework1;

public class homework1 {
	public static void main(String[] args) {
		int terms = 5_000_000;
        double sum = 0.0;

        for (int k = 0; k < terms; k++) {
            double term = 1.0 / (2 * k + 1);
            if (k % 2 == 0) {
                sum += term;
            } else {
                sum -= term;
            }
        }

        double pi = sum * 4.0;

        System.out.printf("계산된 원주율: %.6f\n", pi);
    }
}
```
### Homework6
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

### Homework8
```java

	public class homework {
		    public static void main(String[] args) {
		        int students = 30; 
		        int subjects = 4;  

		        int[][] score = new int[students][subjects];

		        for (int i = 0; i < students; i++) {
		            for (int j = 0; j < subjects; j++) {
		                score[i][j] = (int) (Math.random() * 101);
		            }
		        }

		        System.out.println("=====================================================");
		        System.out.printf("%-4s\t%-4s\t%-4s\t%-4s\t%-4s\t%-5s\t%-5s%n", 
		                          "번호", "국어", "영어", "수학", "과학", "총점", "평균");
		        System.out.println("=====================================================");

		        for (int i = 0; i < students; i++) {
		            int sum = 0;

		            System.out.printf("%2d번\t", (i + 1));

		            for (int j = 0; j < subjects; j++) {
		                System.out.printf("%3d\t", score[i][j]);
		                sum += score[i][j];
		            }

		            double avg = (double) sum / subjects;

		            System.out.printf("%4d\t%5.1f%n", sum, avg);
		        }
		        System.out.println("=====================================================");
		    }
		}

```
