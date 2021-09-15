# Kadane
Kadane’s algorithm is an iterative dynamic programming algorithm in which we search for a maximum sum contiguous subarray within a one-dimensional numeric array. Now, let us see how Kadane’s Algorithm works. Working of Kadane’s Algorithm Some of you may think it’ll be a sum of all elements in an array.


### Questions

* [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
```js
/**
 * @param {number[]} nums
 * @return {number}
 */
var maxSubArray = function(nums) {
    if (nums.length === 0) return 0;

    let max = nums[0];
    let sum = 0;
    for (const num of nums) {
        sum = num + sum;
        max = Math.max(sum, max)
        if (sum < 0) sum = 0
    }

    return max
};
```

### Reference
* [Kadane's - GeeksForGeeks](https://practice.geeksforgeeks.org/problems/kadanes-algorithm-1587115620/1)