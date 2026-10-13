
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

### Homework7
```java

	public class homework {
		    public static void main(String[] args) {
		        int data[] = new int[20];
		        for (int i = 0; i < 20; i++)
		            data[i] = (int)(Math.random() * 100);

		        System.out.println("정렬 전");
		        for (int i = 0; i < 20; i++)
		            System.out.print(data[i] + " ");
		        System.out.println();

		        // 선택 정렬 (Selection Sort)
		        for (int i = 0; i < 19; i++) {
		            int min = i;
		            for (int j = i + 1; j < 20; j++) {
		                if (data[j] < data[min])
		                    min = j;
		            }
		            int temp = data[i];
		            data[i] = data[min];
		            data[min] = temp;
		        }

		        System.out.println("정렬 후");
		        for (int i = 0; i < 20; i++)
		            System.out.print(data[i] + " ");
		        System.out.println();
		    }
		}
```
<img width="1300" height="487" alt="소팅알고리즘출력" src="https://github.com/user-attachments/assets/6c19fd13-bdae-4fbd-b058-3b2773b5736d" />


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


### Homework10
```java

	public class homework {
		public static void main(String[] args) {
			// TODO Auto-generated method stub
			int array_count, max_value, bin_size, display_scale, hist_size;
			if(args.length !=4)
				return;
			array_count = Integer.parseInt(args[0]);
			max_value = Integer.parseInt(args[1]);
			bin_size = Integer.parseInt(args[2]);
			display_scale = Integer.parseInt(args[3]);
			hist_size = max_value/bin_size;
			
			int[] arr = new int[array_count];
			int[] hist = new int[hist_size];
			for (int i=0; i<array_count; i++) {
				arr[i] = (int) (Math.random()*max_value);
			}
			for (int i=0; i<array_count; i++) {
				System.out.print(arr[i] + " ");  
			}
			System.out.println();  
			
			for (int i=0; i<array_count; i++) {
				hist[arr[i]/bin_size]++;
			}
			for (int i=0; i<hist_size; i++) {
				System.out.print(hist[i] + " ");  
			}
			System.out.println();  
		}
	}
```

<img width="1550" height="671" alt="도수분포표만들기" src="https://github.com/user-attachments/assets/e560e5be-f00b-4071-bbc3-7d60c17c4dbe" />




