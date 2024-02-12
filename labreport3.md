# Lab Report 3
<br> *Part 1*
<br>
<br> Below is the code for a buggy program.
<br> ![Image](buggyprogram.png)
<br>
<br> A failure-inducing input for the buggy program
- ```double[] input2 = { 1.0 , 1.0, 2.0, 4.0 };```
- ```assertEquals( 3.0 , ArrayExamples.averageWithoutLowestBuggy(input2), 0.0);```  

An input that doesn't induce a failure
- ```double[] input1 = { 1.0, 2.0, 3.0 };```
- ```assertEquals( 2.5 , ArrayExamples.averageWithoutLowestBuggy(input1), 0.0);```

The symptom, as the output of running the tests
<br> ![Image](bug.png)  

<br> The bug  
Before:
-     static double averageWithoutLowestBuggy(double[] arr) {
          if(arr.length < 2) { return 0.0; }
          double lowest = arr[0];

          for(double num: arr) {
            if(num < lowest) { lowest = num; }
          }

          double sum = 0;
  
          for(double num: arr) {
            if(num != lowest) { sum += num; }
          }
          return sum / (arr.length - 1);
      }
After:
-     static double averageWithoutLowest(double[] arr) {
        if(arr.length < 2) { return 0.0; }
        double lowest = arr[0];

        for(double num: arr) {
          if(num < lowest) { lowest = num; }
        }

        double sum = 0;
        double counter = 0;

        for(double num: arr) {
          if(num != lowest) { 
            sum += num; 
            counter +=1 ;
          }
        }
        return sum / (counter);
      }
The fix was adding a counter that wasn't connected to the length of the array. Because some of the arrays may have repeated lowest integers,
we needed to account for that. With the counter, the code will be able to keep track of the sum and number of integers without the repeated lowest integers.  

*Part 2: Researching Commands*  
<br> I chose ```find``` as my command.  
