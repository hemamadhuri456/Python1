class Solution:
    def findDuplicates(self, nums: List[int]) -> List[int]:
        seen=set()
        ans=set()

        for i in nums:
            if(i in seen):
                ans.add(i)
            else:
                seen.add(i)
                
        return list(ans)
        
