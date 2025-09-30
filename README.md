# leetcode----2221
Find Triangular Sum of an array
//code in kotlin
class Solution {
    fun triangularSum(nums: IntArray): Int {
        val n = nums.size
        val arr = nums.copyOf()  

        for (size in n downTo 2) {
            for (i in 0 until size - 1) {
                arr[i] = (arr[i] + arr[i + 1]) % 10
            }
        }

        return arr[0]
    }
}
