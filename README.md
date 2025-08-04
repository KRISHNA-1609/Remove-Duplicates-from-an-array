# Remove-Duplicates-from-an-array
class Solution {
    public int removeDuplicates(int[] nums) {
        int i=0;
        for(int j=1;j<nums.length;j++){
            if(nums[i]<nums[j]){
                int temp = nums[i+1];
                nums[i+1] = nums[j];
                nums[j] = temp;
                i++;
            }
        }
        return i+1;
    }
    public static void main(String [] args){
        Solution S = new Solution();
        int [] nums = new int[] {1,1,2,2,2,3,3,4};
        S.removeDuplicates(nums);
    }
}
