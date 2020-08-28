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
        for (let j=0; j<(n-i-1); j++){
            if(inputArr[j]>inputArr[j+1]){
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