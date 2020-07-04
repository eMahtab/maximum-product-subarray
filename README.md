# Maximum Product Subarray
## https://leetcode.com/problems/maximum-product-subarray


# Implementation : O(N ^ 2)
```java
class Solution {
    public int maxProduct(int[] nums) {
        if(nums == null || nums.length == 0)
            return 0;
        int maxProduct = nums[0];
        for(int i = 0; i < nums.length; i++) {
            int product = 1;
            for(int j = i; j < nums.length; j++) {
                product *= nums[j];
                maxProduct = Math.max(maxProduct, product);
            }
        }
        return maxProduct;
    }
}
```
