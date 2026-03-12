class Solution:
    def minMoves2(self, nums: List[int]) -> int:
        nums.sort()
        length = len(nums)
        middleElement = nums[length // 2]
        total = 0
        for num in nums:
            total += abs(num - middleElement)
        return total
