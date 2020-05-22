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
def insert(self, intervals, newInterval):
    result = []
    inserted = False
    for interval in intervals:
        if(inserted):
            result.append(interval)
        elif(interval[1] < newInterval[0]):
            result.append(interval)
        elif(newInterval[1] < interval[0]):
            result.append(newInterval)
            result.append(interval)
            inserted = True
        else:
            newInterval[0] = min(newInterval[0], interval[0])
            newInterval[1] = max(newInterval[1], interval[1])
    if(not inserted):
        result.append(newInterval)
    return result    
        
```
        


