class Solution:
    def smallestGoodBase(self, n: str) -> str:
        n = int(n)
        
        # Try all possible lengths of representation from high to low
        for m in range(64, 1, -1):
            # Try to find base k using binary search
            low, high = 2, int(n ** (1 / (m - 1))) + 1
            while low <= high:
                k = (low + high) // 2
                # Use geometric progression sum formula
                total = (k ** m - 1) // (k - 1)
                if total == n:
                    return str(k)
                elif total < n:
                    low = k + 1
                else:
                    high = k - 1
                    
        # If no base found, then the number itself is made of two 1's in base n-1
        return str(n - 1)
