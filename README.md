# Leetcode_3-8-2023-prblm-solutions
# Running Sum of 1d Array
Given an array nums. We define a running sum of an array
as runningSum[i] = sum(nums[0]…nums[i]).
Return the running sum of nums.

Solution:
Java:
class Solution {
    public int[] runningSum(int[] nums) {
        int sum=0;
        int runningsum[]=new int[nums.length];
        for(int i=0;i<nums.length;i++)
        {
            sum=sum+nums[i];
            runningsum[i]=sum;
        }
        return runningsum;
    }
}
# Sum of All Odd Length Subarrays
Given an array of positive integers arr, return the sum of
all possible odd-length subarrays of arr.
A subarray is a contiguous subsequence of the array.

Solution :
class Solution {
    public int sumOddLengthSubarrays(int[] arr) {
        int s,e,tot,odd,sum=0;
        for(int i=0;i<arr.length;i++)
        {
            s=arr.length-i;
            e=i+1;
            tot=s*e;
            odd=tot/2+tot%2;
            sum+=odd*arr[i];
        }
        return sum;
    }
}

#Find the Highest Altitude
There is a biker going on a road trip. The road trip consists
of n + 1 points at different altitudes. The biker starts his
trip on point 0 with altitude equal 0.
You are given an integer array gain of length n where
gain[i] is the net gain in altitude between points i and i + 1
for all (0 <= i < n). Return the highest altitude of a point.

Solution:
class Solution {
    public int largestAltitude(int[] gain) {
        int sum=gain[0];
        int max=0;
        for(int i=1;i<gain.length;i++)
        {
           if(max<sum)
           {
               max=sum;
           }
           sum+=gain[i];
        }
        if(sum>max)
        {
            max=sum;
        }
        return max;
    }
}

#Find the Middle Index in Array
Given a 0-indexed integer array nums, find the leftmost
middleIndex (i.e., the smallest amongst all the possible
ones).

Solution : 
