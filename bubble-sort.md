# Bubble Sort

![Algorithm](src/Bubble-sort.gif)

## Python
```python
def bubbleSort(array):
    n = len(array)
    for i in range(n):
        for j in range(0, n-i-1):
            if array[j] > array[j+1]:
                array[j], array[j+1] = array[j+1], array[j]

array = [190, 1200, 1, 2, 4, 55, 1000, 6, 800]
bubbleSort(array)

for i in range(len(array)):
    print("%d"%array[i])
```

## Javascript
```javascript
bubbleSort = (inputArr) => {
    let n = inputArr.length;
    for (let i=0; i<n; i++){
        for (let j=0; j < (n-i-1); j++){
            if(inputArr[j] > inputArr[j+1]){
                let tmp = inputArr[j];
                inputArr[j] = inputArr[j + 1];
                inputArr[j + 1] = tmp;
            }
        }
    }
    return inputArr;
}

let array = [190, 1200, 1, 2, 4, 55, 1000, 6, 800];
bubbleSort(array).map(a =>{
    console.log(a);
})
```

##  C++
```c++
#include <iostream>
using namespace std;

void swap(int *xp, int *yp){
    int temp = *xp;
    *xp = *yp;
    *yp = temp;
}

void bubbleSort(int arr[], int n){
    int i, j;
    for (i = 0; i < n-1; i++)
        for (j = 0; j < n-i-1; j++)
            if (arr[j] > arr[j+1])
                swap(&arr[j], &arr[j+1]);
}

void printArray(int arr[], int size){
    int i;
    for (i = 0; i < size; i++)
        cout << arr[i] << " ";
    cout << endl;
}

int main(){
    int arr[] = {190, 1200, 1, 2, 4, 55, 1000, 6, 800};
    int n = sizeof(arr)/sizeof(arr[0]);
    bubbleSort(arr, n);
    cout << "Sorted array: \n";
    printArray(arr, n);
    return 0;
}
```

## Go
```go
package main

import "fmt"

func BubbleSort(numbers []int){
    n := len(numbers)
    for i:=0;  i < n; i++{
        for j:=0; j < n-i-1; j++{
            if numbers[j] > numbers[j+1]{
                numbers[j], numbers[j+1] = numbers[j+1], numbers[j]
            }
        }
    }
}

func main(){
    array := []int {190, 1200, 1, 2, 4, 55, 1000, 6, 800}
    BubbleSort(array)
    fmt.Println(array)
}
```