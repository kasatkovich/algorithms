# intervals
+[Insert interval](#insert-interval)
+[Merge intervals](#merge-intervals)
+[Non-overlapping Intervals](#non-overlapping-intervals)

## non-overlapping intervals

https://leetcode.com/problems/non-overlapping-intervals/submissions/

## merge intervals

https://leetcode.com/problems/merge-intervals/

## insert interval

https://leetcode.com/problems/insert-intervals/
    
    
    def insert(self, intervals, newInterval):
        result = []
        inserted = False
        
        for interval in intervals:
            if(inserted):
                result.append(interval)
            elif(interval[1] < newInterval[0]):
                #interval is to left of newInterval
                result.append(interval)
            elif(newInterval[1] < interval[0]):
                #newInterval is to left of interval
                result.append(newInterval)
                result.append(interval)
                inserted = True
            else:
                #interval and newInterval overlap
                #update newInterval
                newInterval[0] = min(newInterval[0], interval[0])
                newInterval[1] = max(newInterval[1], interval[1])
        
        if(not inserted):
            result.append(newInterval)
        
        return result
        


