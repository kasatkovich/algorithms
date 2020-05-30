# intervals
+[Insert interval](#insert-interval)
+[Merge intervals](#merge-intervals)
+[Non-overlapping Intervals](#non-overlapping-intervals)

## non-overlapping intervals

https://leetcode.com/problems/non-overlapping-intervals/

```python
def eraseOverlapIntervals(self, intervals: List[List[int]]) -> int:
    if not intervals:
        return 0
    numNonOverlapping = 1
    intervals.sort(key=lambda x: x[1])
    endHolder = intervals[0][1]
    for interval in intervals:
        if interval[0] >= endHolder:
            numNonOverlapping += 1
            endHolder = interval[1]
    return len(intervals) - numNonOverlapping

```

## merge intervals

https://leetcode.com/problems/merge-intervals/

```python
def merge(self, intervals: List[List[int]]) -> List[List[int]]:
    if not intervals:
        return intervals
    intervals.sort(key=lambda x: x[0])
    heap = []
    for interval in intervals:
        if heap and heap[-1][1] >= interval[0]:
            heap[-1][1] = max(heap[-1][1], interval[1])
        else:
            heap.append(interval)
    return heap

```

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
        


