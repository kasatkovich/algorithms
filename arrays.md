# Arrays
+[Two Sum](#two-sum)
+[3Sum](#3Sum)
+[Subarray Sum Equals K](#subarray-sum-equals-k)

## Two Sum
https://leetcode.com/problems/two-sum/

```python
def twoSum(self, nums: List[int], target: int) -> List[int]:
    x = []
    nums = enumerate(nums)
    nums = sorted(nums, key=lambda x: x[1])
    l = 0
    r = len(nums)-1
    while l < r:
        if nums[l][1] + nums[r][1] == target:
            x.append(nums[l][0])
            x.append(nums[r][0])
            return x
        elif nums[l][1] + nums[r][1] > target:
            r -= 1
        elif nums[l][1] + nums[r][1] < target:
            l += 1


```                

## 3Sum
https://leetcode.com/problems/3sum/

## Subarray Sum Equals K
https://leetcode.com/problems/subarray-sum-equals-k/v



