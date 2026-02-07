# PACE
For education purposes 
copied the code from leetcode 
#include <vector>
#include <unordered_map>
using namespace std;

    class Solution {
    p:ublic:
    vector<int> intersect(vector<int>& nums1, vector<int>& nums2) {
        unordered_map<int, int> freq;
        vector<int> result;

        // Count frequency of nums1
        for (int num : nums1) {
            freq[num]++;
        }

        // Check against nums2
        for (int num : nums2) {
            if (freq[num] > 0) {
                result.push_back(num);
                freq[num]--;
            }
        }

        return result;
    }
};
