# Quiz 3 Corrections
2. Complete the trace table for each variable in the following code segment.
```
int i = 1, j = 2, count = 1;
while (count < 3){
    i = i + j;
    j = i - j;
    count++;
}
```
**Answer**:

| `i` | `j` | `count` |
|-----|-----|---------|
|1    |2    |1        |
|3    |1    |2        |
|4    |3    |3        |

**Correction**:
```
I got the wrong 2nd value of j wrong as I thought the value of i would not change until after the loop iteration had passed, so I thought i would stay as 1 even after it had a newly declared value after the first loop statement. This which lead to the third values of i and j to also be wrong as the while loop goes through its 3rd iteration. 

Instead while count is declared 1, the program goes through the first iteration of the loop with the first statement of i
being declared as i + j, placing their int values, 1 and 2 respectively, and adding them to newly declare the int value i
as 3. The program goes to the next statement with j having the new value from i - j. Using the changed int value of i as
being 3 being subtracted by j's intial declared value: 2. This then gets j to be declared the int value 1. The program then
moves to the next statement, increases the value of count by 1. Count then equals 2.

While count is declared 2, the program goes through its second iteration of the loop with the first statement of i being
declared as i + j, placing their int values, 3 and 1 respectively, and adding them to newly declare the int value i as 4.
The program goes to the next statement with j having the new value from i - j. Using the changed int value of i as being 4
being subtracted by j's value: 1. This then gets j to be declared the int value 3. The program then moves
to the next statement, increases the value of count by 1. Count then equals 3.

The while loop ends as it's boolean condition of the int value count being less than 3 is no longer true.
   
```

7. Write a while loop that finds the sum of the first ten perfect-squares, i.e. find the sum 1^2 + 2^2 + 3^2 + ... + 9^2 +
   10^2.

**Answer**:
```
int i = 1;
int sum = 0;
while (i <= 10) {
   sum += i * i;
   i++;
}
```
**Correction**:
```
I got this problem wrong because I entered 'sum = sum + Math.Pow(i,2)', which returns a double value and results in error
as the while loop has to work with the same value types as the previously declared int i value. I should have instead
entered 'sum += i * i' as in place of my answer as it returns an int value.
```

8. Convert the for loop to a while loop:
```
for (int j = 0; j <= 9; j++){
    System.out.println(j * j);
}
```
**Answer**:
```
int j = 0;
while (j <= 9) {
    System.out.print(j * j);
    j++;
}
```
**Correction**:
```
I put '(j >= 0 && j <=9)' for the boolean statement. I can remove the condition of 'j >= 0' as it is redundant as the while
loop still works without it.
```
9. Create a trace table for the variable in
```
for (int i = 0; i < 7; i++){
    if (i%2 == 0){
        i = i + 2;
    } else {
        i = i * 2;
    }
}
```
**Answer**:

| `i` |
|-----|
|0    |
|2    |
|3    |
|6    |
|7    |

**Correction**:
```
I left the 3rd, 4th, and 5th values of i in the trace table blank. This due to being unable to understand that the trace
table takes into account that i increments by one after an iteration of the loop, so i would go from 2 to its 3rd value of
3. In the next loop iteration, the if statement's boolean is untrue as the remainder of 3 and 2 does not equal 0, so the
program goes to else statement in which i is declared with 3 multiplied by 2. This gets i's 4th value of 6. The loop then
incrementally increases i by 1, so i gets its 5th value of 7. The for loop's condition of 'i < 7' becomes no longer true,
ending the for loop.
```

10. How many iterations are carried out by the following loop?
```
for (int j = 9; j < 50; j = j + 7) {
    if (j % 3 == 0) {
        System.out.println("j = " + j);
    }
}
```
**Answer**:
```
6 (with margin: 0)
```
**Correction**:
```
I thought the for loop would have only 2 iterations as I believed, without reason, that the loop would not iterate when the nested if statement's boolean in the loop was not true. Instead the for loop would keep iterating regardless of the if statement would execute or not. So the for loop would continue with the int value of j increasing by 7 a total of 6 iterations. After the 6th iteration, the value of j would be increased up to 56, which renders the loop's boolean untrue, stopping the loop which then does not execute the if statement's code. 
```

11. How many iterations are carried out by the following loop?
```
for (int j = 1, k = 1; j < 5 || k % 3 == 0; j = j + 2, k++){
    if (j % k == 0) {
        System.out.println(j % k);
    }
}
```
**Answer**:
```
3 (with margin: 0)
```

**Correction**:
```
Much like question 10 I thought the for loop would have only 1 iteration as I believed, without reason, that the loop would not iterate when the nested if statement's boolean in the loop was not true. Instead the for loop would keep iterating regardless of the if statement would execute or not. So the for loop would iterate 3 times, with the first one executing the if statement as one of the loop's boolean statements of j < 5 is true as j is initially declared as 1. In the second iteration, the loop executes again as the boolean of j < 5 is again true after j is increased by 2 to the value of 3. In the third iteration, the boolean is once more true as the value of k is, by this third iteration of the loop, is equal to 3 (after being incremented by 1 over the past 2 loop iterations) through the loop's other boolean statememt of k % 3 == 0. A  fourth iteraton would not come to be as neither boolean statements would be true as j would equal to 7 and k is equal to 4. 
```

12. Write a for loop that prints out the string str in reverse. For example, "bat" would be displayed as tab. Assume str
    has been declared and initialized.
**Answer**:
```
String reverse = "";
for (int i = 0; i  < str.length(); i++) {
    reverse = str.charAt(i) + reverse;
}
System.out.print(reverse);
```
**My Answer**:
```
for (int i = str.length(); i >= 0; i--) {
    System.out.print(str.charAt (i));
}
```
**Correction**:
```
for (int i = str.length() - 1; i >= 0; i--) {
    System.out.print(str.charAt (i));
}
I had forgotten how the charAt() and length() methods functioned as charAt() would take the positions of a string starting from 0 and length() would return the total number of characters in a string. In my old answer, the boolean would always be true as i refers to the string length and the loop checks for i being greater than or equal to 0. The boolean would no longer be always true if i is declared as the string length() and being subtracted 1.
```

13. Write a nested for loop that displays the pattern.
```
X
O X
O O X
O O O X
```
**Answer**:
```
for (int i = 1; i <= 4; i++) {
   for (int j = 1; j <= i; j++) {
      if(i == j) {
         System.out.print("X");
      } else {
         System.out.print("O");
      }
   }
   System.out.println();
}
```
**Correction**:
```
I failed to finish my nested for loop as I had not known how to write a nested for loop.
```























