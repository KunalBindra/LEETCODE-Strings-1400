# Check If a String Can Be Formed by Reorganizing Characters
**Solution:**
class Solution {
    public boolean canConstruct(String s, int k) {
      int n=s.length();
      int occ=0;
      if(n==k) return true;
      if(n<k) return false;
      int[] vec=new int[26];
      for(char ch:s.toCharArray())
      {
        vec[ch-'a']++;
      }  
      for(int i=0;i<26;i++)
      {
        if(vec[i]%2!=0) occ++;
      }
      return occ<=k;
    }
}
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
