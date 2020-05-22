# Arrays
+[Two Sum](#two-sum)
+[3Sum](#3Sum)
+[Subarray Sum Equals K](#subarray-sum-equals-k)

## Two Sum
https://leetcode.com/problems/two-sum/

```python
def twoSum(self, nums: List[int], target: int) -> List[int]:
    hashtable = {};
    for i in range(len(nums)):
        if nums[i] not in hashtable:
            hashtable[target-(nums[i])] = i;
        else:
            return [hashtable[nums[i]], i];
```                

## 3Sum
https://leetcode.com/problems/3sum/

## Subarray Sum Equals K
https://leetcode.com/problems/subarray-sum-equals-k/v



