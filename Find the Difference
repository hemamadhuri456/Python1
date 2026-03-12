class Solution:
    def findTheDifference(self, s: str, t: str) -> str:
        # Solution 5: One Liner
        return chr(sum(map(ord, t)) - sum(map(ord, s)))
        # Time: O(n)
        # Space: O(1)

        # Solution 4: Diff of the Sum of Unicode code values
        extra_code = sum(map(ord, t)) - sum(map(ord, s))
        return chr(extra_code)
        # Time: O(n)
        # Space: O(1)

        # Solution 3: XOR - 1 Loops
        res = ord(t[-1])  # Start with the extra character in t
        for i, c in enumerate(s):     # For each position i in s,
            res ^= ord(c) ^ ord(t[i]) # xor out s[i] and t[i]
        return chr(res)   # res is the ascii of the extra char
        # Time: O(n)
        # Space: O(1)

        # Solution 2: XOR - 2 Loops
        res = 0
        for c in t:
            res ^= ord(c)  # XOR in all code‐points from t
        for c in s:
            res ^= ord(c)  # XOR out all code‐points from s
        return chr(res)
        # Time: O(n)
        # Space: O(1)

        # Solution 1: 
        char_count = [0] * 26
        for char in s:
            char_count[ord(char) - 97] += 1
        for char in t:
            char_count[ord(char) - 97] -= 1
        return chr(char_count.index(-1) + 97)
        # Time: O(n)
        # Space: O(1)
