# Redistribute-Characters-to-Make-All-Strings-Equal

from collections import Counter

class Solution:
    def makeEqual(self, words):
        # Count the occurrences of each character in the words
        char_count = Counter("".join(words))
        
        # Check if all character frequencies are divisible by the number of words
        return all(count % len(words) == 0 for count in char_count.values())

# Example usage:
solution = Solution()

words1 = ["abc", "aabc", "bc"]
print(solution.makeEqual(words1))  # Output: True

words2 = ["ab", "a"]
print(solution.makeEqual(words2))  # Output: False
