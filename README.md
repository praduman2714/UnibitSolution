# Question:

Given an array of integers and a target value, you must determine which two integers' sum
equals the target and return a 2D array. Then merge the array into a single array with sorting (
ascending ) order, in the next step double the target value and find again the combination of
digits (can be multiple digits ) that are equal to the double targeted value and returned into a 2D
array.


Sample Input : [1, 3, 2, 2, -4, -6, -2, 8];

Target Value = 4,

Output: First Combination For “4” : [ [1,3],[2,2],[-4,8],[-6,2] ];

Merge Into a single Array : [-6,-4,1,2,2,2,3,8];

Second Combination For “8” : [ [ 1,3,2,2], [8,-4,2,2],....,[n,n,n,n] ]

# Approach

  - The firstCombination function takes an array of integers (nums) and a target value as input and returns a 2D array containing pairs of numbers from the input array that add up to the target value. It uses a map (HashMap) to store pairs of numbers with their corresponding sum. Duplicates are checked using a set (HashSet) to ensure unique pairs. The result is extracted from the map and returned as a 2D array.

  - The mergeAndSort function takes a 2D array (nums) and converts it into a sorted 1D array. It calculates the size of the resulting array and assigns the values from the 2D array to the 1D array. Finally, it sorts the 1D array using Arrays.sort and returns the sorted array.

  - The doubleCombination function takes an array of integers (nums) and a target value as input. It uses recursion to find all unique combinations of numbers from the input array that add up to twice the target value. It calls the backtrack function, which implements the backtracking algorithm. The unique combinations are stored in a list of lists (ArrayList) and then converted into a 2D array, which is returned as the result.

  - In the main function, the user is prompted to enter the length of the array, the elements of the array, and the target value. The firstCombination function is called to find pairs of numbers that add up to the target. The resulting pairs are printed. The mergeAndSort function is then called to convert the 2D array of pairs into a sorted 1D array, which is printed. Finally, the doubleCombination function is called to find combinations of numbers from the 1D array that add up to twice the target, and the resulting combinations are printed.

The program's overall approach involves finding pairs of numbers and then generating combinations based on those pairs to solve the given problem.




 
