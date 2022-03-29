### Problem - Sort the given array and find the count of maximum possible numbers which were in place(didn't change their positions) even after sorting.

```cpp
int maximumInPlace(vector<int> &arr){
    vector<int> temp;
    
    // Copy the original array into a temp array and sort temp array.
    for(int i = 0; i < arr.size(); i++){
        temp.push_back(arr[i]);
    }
    sort(temp.begin(), temp.end());
    
    int count = 0;
    // Compare the original arr with temp arr to find elements that are inplace after sorting.
    for(int i = 0; i < arr.size(); i++){
        if(arr[i] == temp[i]) count++;
    }
    return count;
}

int main()
{
    vector<int> arr {10, 12, 45, 18, 50};
    
    // Stores the count of numbers that didn't changed there place after sorting 
    //i.e numbers [10,12,50] won't change there positions after sorting as they are already in correct position
    int ans = maximumInPlace(arr);
    cout<<ans;
    
    return 0;
}
```
