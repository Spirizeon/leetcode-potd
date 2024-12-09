https://leetcode.com/problems/special-array-ii/
ATTEMPTED
```cpp
class Solution {
public:
    //function to generate parity_array
    bool generate_parity_array(vector<int> nums,int init,int end){


            for(int i=init;i<end;i++){
                if(nums[i]%2 == nums[i+1]%2){
                    return false;
                }
            }
        return true;
    }

    vector<bool> isArraySpecial(vector<int>& nums, vector<vector<int>>& queries) {
        vector<bool> solutionset;

        //process queries for now then
        for(int i=0;i<queries.size();i++){
            int init = queries[i][0];
            int end = queries[i][1];
            bool flag = generate_parity_array(nums,init,end);
            solutionset.push_back({flag});
        }
    return solutionset;
    }
};
```
