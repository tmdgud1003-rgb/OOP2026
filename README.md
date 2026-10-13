
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
<img width="1273" height="807" alt="계단형식별모양출력" src="https://github.com/user-attachments/assets/23fcd546-1bea-4b22-9cdb-839d3b9f0cef" />
### Homework2
```java

	public class homework {
		public static void main(String[] args) 
		{
		    int n = 20; 

		     int prev = 0, curr = 1;

		    System.out.print(prev + " ");
		    System.out.print(curr + " ");

		    for (int i = 2; i < n; i++) {
		        int next = prev + curr;
		        System.out.print(next + " ");
		        prev = curr;
		        curr = next;
		    }

		    // TODO Auto-generated method stub
		} 
	}
```
<img width="1296" height="388" alt="피보나치수열" src="https://github.com/user-attachments/assets/7b8ab64e-2a55-456a-b705-6c4a08538fcc" />
### Homework3
```java

	public class homework {
		public static void main(String[] args)
		{
		    float val1 = 1;
		    float val2 = 2;

		    for (int i = 0; i < 20; i++) {
		        float value = val2 / val1;
		        System.out.println(val2 + "/" + val1 + " = " + value);
		        float temp = val1;
		        val1 = val2;
		        val2 = temp + val2;
		    }
		}
	}
```
<img width="1255" height="446" alt="황금비율계산출력" src="https://github.com/user-attachments/assets/8376156d-d3bc-40b1-bdc8-fd7e960b55e3" />

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
public class homework {
		public static void main(String[] args) {
		    int i, n = 100, sign = 1;
		    double sum = 0;
		    
		    for (i = 0; i < n; i++) {
		        sum += sign * 1.0 / ((2.0 * i + 1.0) * Math.pow(3.0, i));
		        sign *= -1;
		    }
		    
		    System.out.println(sum * Math.sqrt(12)); 
		}
	}
```
<img width="907" height="250" alt="원주율계산" src="https://github.com/user-attachments/assets/932560e3-849f-4c68-94fe-7668b51f5459" />


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
<img width="1536" height="649" alt="과국영수과학성적출력" src="https://github.com/user-attachments/assets/53f5b2fb-155f-4bfb-b23b-1ddace10f2ac" />


