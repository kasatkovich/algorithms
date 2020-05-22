# Arrays
+[Two Sum](#two-sum)
+[3Sum](#3Sum)
+[Subarray Sum Equals K](#subarray-sum-equals-k)

## Two Sum
https://leetcode.com/problems/two-sum/submissions/

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



