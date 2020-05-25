# intervals
+[Insert interval](#insert-interval)
+[Merge intervals](#merge-intervals)
+[Non-overlapping Intervals](#non-overlapping-intervals)

## non-overlapping intervals

https://leetcode.com/problems/non-overlapping-intervals/submissions/

## merge intervals

https://leetcode.com/problems/merge-intervals/

## insert interval

https://leetcode.com/problems/insert-interval/submissions/
    
```python   
def insert(self, intervals: List[List[int]], newInterval: List[int]) -> List[List[int]]:
    intervals.append(newInterval)
    intervals.sort()
    merged = []
    for interval in intervals:
        if not merged or merged[-1][1] < interval[0]:
            merged.append(interval)
        else:
            merged[-1][1] = max(merged[-1][1], interval[1])
    return merged    
        
```
        


