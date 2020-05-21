# Arrays
+[Two Sum](#two-sum)
+[3Sum](#3Sum)
+[Subarray Sum Equals K](#subarray-sum-equals-k)

## Two Sum
https://leetcode.com/problems/two-sum/submissions/

## 3Sum
https://leetcode.com/problems/3sum/

## Subarray Sum Equals K
https://leetcode.com/problems/subarray-sum-equals-k/v

'''python
def subarraySum(self, nums: List[int], k: int) -> int:
        sumMap = {0: 1}
        sumNums = 0
        kSubarrays = 0
        for i in range(len(nums)):
            sumNums += nums[i]
            if sumNums - k in sumMap:
                kSubarrays += sumMap[sumNums - k]
            if sumNums not in sumMap:
                sumMap[sumNums] = 1
            else:
                sumMap[sumNums] += 1
        return kSubarrays
'''



