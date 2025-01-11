# Check If a String Can Be Formed by Reorganizing Characters

**Description:**

This Java class implements a solution to the problem of determining whether a given string can be formed by reorganizing its characters such that no two adjacent characters are the same.

**Solution:**

The `canConstruct` method checks if the given string `s` can be reorganized to meet the condition where no two adjacent characters are the same. 

1. **Initialization:**
   - `n`: Length of the input string `s`.
   - `occ`: Counter for the number of characters with odd occurrences.
   - Check base cases:
     - If `n` is equal to `k` (where `k` is the maximum number of allowed adjacent duplicate characters, which is 1 in this case), it's always possible to reorganize.
     - If `n` is less than `k`, it's impossible to reorganize.

2. **Character Frequency Count:**
   - Create a frequency array `vec` to store the count of each character in the string.

3. **Count Characters with Odd Occurrences:**
   - Iterate through the frequency array and increment `occ` for each character with an odd occurrence.

4. **Check for Feasibility:**
   - If the number of characters with odd occurrences (`occ`) is greater than `k` (which is 1 in this case), it's impossible to reorganize the string. 
   - If `occ` is less than or equal to `k`, it's possible to reorganize the string.

**Time Complexity:**

- O(n), where n is the length of the string.

**Space Complexity:**

- O(1), as the space used by the `vec` array is constant (26 characters).
