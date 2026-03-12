class Solution(object):
    def findComplement(self, num):
        
        compliment = 1
        while compliment <= num:
            compliment = compliment << 1
        
        leftCompliment=compliment - 1
        compliment=(leftCompliment) ^ num
        
        return compliment
        
