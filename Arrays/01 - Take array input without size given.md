## Problem - Perform linear search and return the index where given key is present. Take array as an input without size given.

```cpp
int main()
{
    // Allocating array dynamically
    int *arr[1000], i = 0, sizeofArr = 0;
    
    // Keep taking input until we hit a new line i.e '\n'
    while(1){
        arr[i] = new int;
        cin>>*arr[i];
        
        if(cin.get() == '\n'){
            break;
        }
        
        i++;
        sizeofArr++;
    }
    
    // take input 'key' to be searched in array
    int key;
    cin>>key;
    
    for(int i = 0; i <= sizeofArr; i++){
        if(*arr[i] == key){
            cout<<"Key "<<key<<" found at index: "<<i;
            break;
        }
    }

    return 0;
}
```
