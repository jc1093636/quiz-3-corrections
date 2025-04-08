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

```

7. Write a while loop that finds the sum of the first ten perfect-squares, i.e. find the sum 1^2 + 2^2 + 3^2 + ... + 9^2 + 10^2.

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
```
| `i` |
|-----|
|0    |
|2    |
|3    |
|6    |
|7    |
```
**Correction**:

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

```

12. 

**Answer**:
```

```
**Correction**:
```

```

13. 

**Answer**:
```

```
**Correction**:
```

```























