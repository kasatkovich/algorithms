# intervals
+[Insert interval](#insert-interval)
+[Merge intervals](#merge-intervals)
+[Non-overlapping Intervals](#non-overlapping-intervals)

## non-overlapping intervals

https://leetcode.com/problems/non-overlapping-intervals/submissions/

## merge intervals

https://leetcode.com/problems/merge-intervals/


    def merge(self, intervals: List[List[int]]) -> List[List[int]]:
        if not intervals:
            return intervals
        
        intervals.sort(key = lambda x: x[0])
        stack = []
        
        for interval in intervals:
            if stack and stack[-1][1] >= interval[0]:
                stack[-1][1] = max(stack[-1][1],interval[1])
            else:
                stack.append(interval)
                
        return stack

## insert interval

https://leetcode.com/problems/insert-interval/
