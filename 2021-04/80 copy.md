## 80. 删除有序数组中的重复项 II

```
function removeDuplicates(nums: number[]): number {
    if(nums.length < 2) {
        return nums.length;
    }
    let left = 2, right = 2;
    while(right < nums.length) {
        if(nums[right] != nums[left - 2]) {
            nums[left] = nums[right];
            ++left;
        }
        ++right;
    }
    return left;
};
```