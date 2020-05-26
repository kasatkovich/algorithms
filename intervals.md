# intervals
+[Insert interval](#insert-interval)
+[Merge intervals](#merge-intervals)
+[Non-overlapping Intervals](#non-overlapping-intervals)

## non-overlapping intervals

https://leetcode.com/problems/non-overlapping-intervals/submissions/

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

https://leetcode.com/problems/insert-interval/
