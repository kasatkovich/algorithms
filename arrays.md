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

```python
def threeSum(self, nums):
        result = []
        if len(nums) < 3:
            return result
        num = sorted(nums)
        for i in range(len(num)-2):
            if i == 0 or num[i] > num[i-1]:
                negate = - num[i]
                start = i + 1
                end = len(num) - 1
                while start < end:
                    if num[start] + num[end] == negate:
                        result.append([num[i], num[start], num[end]])
                        start += 1
                        end -= 1
                        while start < end and num[end] == num[end+1]:
                            end -= 1
                        while start < end and num[start] == num[start-1]:
                            start += 1
                    elif num[start] + num[end] < negate:
                        start += 1
                    else:
                        end -= 1
        return result

```
## Subarray Sum Equals K
https://leetcode.com/problems/subarray-sum-equals-k/v

```python
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

```



