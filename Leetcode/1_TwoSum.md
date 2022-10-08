<b>Problem</b>: 1. Two Sum </br>
<b>Description: </b> Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.</br>

You may assume that each input would have exactly one solution, and you may not use the same element twice.</br>

You can return the answer in any order.</br>

<b>Examples: </b>
```
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].
```

```
Input: nums = [3,2,4], target = 6
Output: [1,2]
```

```
Input: nums = [3,3], target = 6
Output: [0,1]
```

<b>Solution 1:</b></br>
![Solution 1](./images/Solution%201.gif)
</br>
```
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        length = len(nums)
        for i in range(length):
            for j in range(i + 1, length):
                if nums[i] + nums[j] == target:
                    return [i, j]
```
<b>Time Complexity:</b> O(n^2)