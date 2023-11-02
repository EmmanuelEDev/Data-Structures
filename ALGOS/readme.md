## Problem 1

# Distinct Elements Algorithm

This is an algorithm designed to find and sum distinct elements from two sets represented as arrays. It counts the elements in the first set that are not present in the second set and vice versa, then computes the sum of these distinct elements.

## Algorithm Description

The algorithm performs the following steps:

1. Initialize two arrays, Set1 and Set2, to store the input sets.
2. Initialize variables sum, sum1, sum2, i, j, and count.
3. Loop through the elements in Set1 and Set2 to find distinct elements.
   - For each element in Set1, check if it exists in Set2 by iterating through Set2.
   - If an element in Set1 is not found in Set2, increment the count.
   - If the count reaches the length of Set2, the element in Set1 is distinct. Add it to sum1.
   - Repeat the same process for Set2, counting elements not present in Set1 and adding them to sum2.
4. Calculate the total sum of distinct elements as `sum1 + sum2`.
5. Output the sum to the console.

## Variables

- `Set1`: An array of integers representing the first set.
- `Set2`: An array of integers representing the second set.
- `sum`: The total sum of distinct elements.
- `sum1`: The sum of distinct elements in Set1.
- `sum2`: The sum of distinct elements in Set2.
- `i`: Loop variable.
- `j`: Loop variable.
- `count`: A counter to keep track of distinct elements.

## Usage

You can use this algorithm to find and sum distinct elements from two sets. Simply provide the sets as input arrays and run the algorithm. The result will be the sum of the distinct elements.

## Example

```python
VAR
    Set1 : ARRAY_OF INTEGER[4];
    Set2 : ARRAY_OF INTEGER[5];
    sum, sum1, sum2, i, j, count : INTEGER := 0
BEGIN
    Set1 := {3,1,7,9}
    Set2 := {2,4,1,9,3}

    ... (Algorithm code as provided)

    Write("The sum is:" sum)
END


## Problem 2

# Dot Product (Orthogonal Vectors) Algorithm

This algorithm calculates the dot product of two vectors and determines whether they are orthogonal (perpendicular) or not. The dot product result is computed, and based on whether it is equal to zero or not, the algorithm determines if the vectors are orthogonal.

## Algorithm Description

The algorithm performs the following steps:

1. Initialize two arrays, `v1` and `v2`, to represent the two vectors.
2. Initialize variables `sum` and `i` to zero to accumulate the dot product result.
3. Loop through the elements of the arrays `v1` and `v2` to calculate the dot product by multiplying corresponding elements and accumulating the result in the `sum` variable.
4. Check if the dot product result is equal to zero:
   - If the result is zero, it means the vectors are orthogonal, and a message is displayed.
   - If the result is not zero, it means the vectors are not orthogonal, and a different message is displayed.
5. Finally, the algorithm outputs the dot product result to the console.

## Variables

- `v1`: An array representing the first vector.
- `v2`: An array representing the second vector.
- `sum`: The result of the dot product.
- `i`: Loop variable.

## Usage

You can use this algorithm to calculate the dot product of two vectors and determine if they are orthogonal. Provide the vectors as input arrays, and the algorithm will compute and display the result.

## Example

```python
VAR
    v1 : ARRAY_OF INTEGER[5];
    v2 : ARRAY_OF INTEGER[5];
    sum, i: INTEGER := 0
BEGIN
    v1 := {9, 4, 2, 0, 7};
    v2 := {7, 0, 8, 1, 6};

    FOR i FROM 0 TO 4 DO
        sum := sum + (v1(i) * v2(i))
        
        IF (sum = 0) THEN
            Write("This pair of vectors is orthogonal");
        ELSE
            Write("This pair of vectors is not orthogonal");
        END_IF
    END_FOR

    Write("Dot Product Result: " + sum)
END


