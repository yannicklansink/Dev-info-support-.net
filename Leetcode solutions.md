[Programming Skills - Study Plan - LeetCode](https://leetcode.com/studyplan/programming-skills/)

29-4-23 | 1768. Merge Strings Alternately
**Input:** word1 = "abcd", word2 = "pq"
**Output:** "apbqcd"
```csharp
public class Solution {
    public string MergeAlternately(string word1, string word2) {
        StringBuilder res = new StringBuilder();
        int i = 0, j = 0;
        while (i < word1.Length && j < word2.Length) {
            res.Append(word1[i]).Append(word2[j]);
            i++;
            j++;
        }

        while (i < word1.Length) {
            res.Append(word1[i]);
            i++;
        }

        while (j < word2.Length) {
            res.Append(word2[j]);
            j++;
        }

        return res.ToString();
    }
}
```
