# Part 1: Debugging scenario


1. The original post from student:

Hi, I am currently working on this method that calculates the average of an array without including the lowest number in the array.
However, I am not getting the correct output the output that i'm getting from entering an array is lower than the average expected. I'm guessing that i am incorrectly calculating a part of the sum. With the inputed array the average was supposed to be 35.0 but 30.0 was ouputed. 

<img width="525" alt="Screenshot 2024-03-12 at 11 17 35 PM" src="https://github.com/AdeyAA/cse15l-lab-reports/assets/96445037/3fa06886-8184-43e1-8089-dc56df375dac">

<img width="385" alt="Screenshot 2024-03-12 at 11 29 09 PM" src="https://github.com/AdeyAA/cse15l-lab-reports/assets/96445037/4b391481-6b0d-4ca3-8f03-1906df0d59c5">




   
2. A response from a TA:



Hi, your method is on the right track, currently, the second loop iterates through the doubles in the array and sums up all of the doubles that are included in the array. But your objective is to exclude the lowest number from the sum. How do you think you could add this step to your second for loop? Think of ways to exclude a certain number from being added to the sum. 




3. Screenshot of output that the student got:

<img width="551" alt="Screenshot 2024-03-12 at 11 15 38 PM" src="https://github.com/AdeyAA/cse15l-lab-reports/assets/96445037/23350bd1-3dd4-4065-b916-4e6b58e7227c">


<img width="387" alt="Screenshot 2024-03-12 at 11 27 51 PM" src="https://github.com/AdeyAA/cse15l-lab-reports/assets/96445037/c180b171-7630-4c86-b835-68db12dba3e9">


Thank you for the help. The bug was in my second for loop like you suggessted, what I was missing was only adding the number `num` if it is not equal to the number `lowest` so I added an `if` statement to check if `num` is not equal to `lowest` then we should only add it to the `sum` of the array. Also I added that the `sum` should be divided by `arr.length - 1` becasue we excluded a number from the `sum` which makes the array smaller by 1.


4. The file & directory structure needed:

lab-report/
│
├── AverageCalculator.java
└── test.sh


   
The contents of each file before fixing the bug:

Average Calculator file:

```
public class AverageCalculator {
  static double averageWithoutLowest(double[] arr) {
    if (arr.length < 2) {
      return 0.0;
    }
    double lowest = arr[0];
    for (double num : arr) {
      if (num < lowest) {
        lowest = num;
      }
    }
    double sum = 0;
    for (double num : arr) {
      sum += num;
    }
    return sum / arr.length;
  }

  public static void main(String[] args) {
    double[] nums = { 10, 20, 30, 40, 50 };
    System.out.println("Average: " + averageWithoutLowest(nums));

  }
}

```
test.sh contents:

```
javac AverageCalculator.java
java AverageCalculator
```




The full command line (or lines) you ran to trigger the bug:


```
adey@Adeys-MacBook-Pro lab-report-a % bash test.sh
Average: 30.0
```





A description of what to edit to fix the bug:

The second for loop needed to be edited. So first I began by adding an `if` statement checking ` num != lowest` then add the `num` to the `sum` and then the return statment was fixed to `return sum / (arr.length - 1)`. 





# Part 2: Reflection:

Some cool things I learned in the second half of the quarter is how to edit files using vim also being able to add things to files and creat directories using the command line.


