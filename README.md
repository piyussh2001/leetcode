# leetcode
practising leetcode question to improve coding



2200.find all the k distant elements in array

       class Solution {
        public:
    vector<int> findKDistantIndices(vector<int>& nums, int key, int k) {
        vector<int> keyIndices;
        vector<int> result;
        for (int i = 0; i < nums.size(); ++i) {
            if (nums[i] == key) {
                keyIndices.push_back(i); // 2   5
            }
        }

          for (int i = 0; i < nums.size(); i++) { // 0 to 6
            for (int index : keyIndices) {
                if (abs(i - index) <= k) {
                    result.push_back(i);
                    break;  
                }
            }
        }
    return result;
    }
     };
2.two sum

    class Solution {
    public:
    vector<int> twoSum(vector<int>& nums, int target) {
        vector<int> result;
        for(int i=0;i<nums.size();i++)
        {
        for(int j=i+1;j<nums.size();j++)
        {
            if(nums[i]+nums[j]==target)
            {
                result.push_back(i);
                result.push_back(j);
                 return result;
            }
        }
        }
        return result;
        
    }
};
