# 88.Merge Sorted Array

**Problem:**

Given two sorted integer arrays nums1 and nums2, merge nums2 into nums1 as one sorted array.

    //What is the point of this part!!!!!!
    Note:

    You may assume that nums1 has enough space (size that is greater or equal to m + n) to hold additional elements from nums2. 

    The number of elements initialized in nums1 and nums2 are m and n respectively.
    
    
    
    
** My solutions:**

Date: March 30, 2016

    class Solution {
    public:
        void merge(vector<int>& nums1, int m, vector<int>& nums2, int n) {
            nums1.resize(m+n);
            cout<<nums1.size()<<endl;
            vector<int>::iterator iter1 = nums1.begin(),iter2 = nums2.begin();
            while(iter2!=nums2.end()){
                if(*iter2<=*iter1){
                    nums1.insert(iter1, *iter2);
                    iter2++;
                    iter1--;
                } 
                else{
                    iter1++;
               }
            }
        }
    };