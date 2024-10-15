# EXP-19

## Aim:
**To study and implement sorting algorithm C++.**

## Software:
`Microsoft VSCode`

## Theory:
Sorting algorithms are used to rearrange elements of a list in a specific order, typically either ascending or descending. Below, I'll explain a few common sorting algorithms in C++.
Bubble Sort Bubble Sort repeatedly compares adjacent elements and swaps them if they are in the wrong order. This process is repeated until the list is sorted.

Selection Sort Selection Sort finds the minimum element from the unsorted part of the list and swaps it with the first unsorted element. It repeats this process until the list is sorted.

Insertion Sort Insertion Sort builds the sorted list one item at a time by repeatedly taking one unsorted item and inserting it into the correct position within the sorted part of the list.





## Code: 20A
(A) <br> 
```cpp
// NAME - Kanwaljeet singh
//PRN - 23070123124 
// EXPERIMET - 20(A) 

#include<iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void s_sort(int *a, int elements) {
    int n = 0;
    int *b;

    while (n < elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}

int main() {
    int no_el;
    cout << "How many elements in your array?" << endl;
    cin >> no_el;
    int arr[no_el];

    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cin >> arr[i];
    }

    s_sort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    return 0;
}
```

## Output:
![image](https://github.com/user-attachments/assets/da1c187d-6509-4399-ba42-58390c09d0ca)









## Code: 20B
```cpp
// NAME - Kanwaljeet singh
// PRN - 23070123124
// EXPERIMENT - 20(B) 

#include<iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void bubbleSort(int *a, int elements) {
    int n = 0;
    int *b;

    while (n < elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}

int main() {
    int no_el;
    cout << "How many elements in your array?" << endl;
    cin >> no_el;

    int arr[no_el];
    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cin >> arr[i];
    }

    bubbleSort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;

    return 0;
} 
```

## Code: 20C
```cpp
// NAME - Kanwaljeet singh
// PRN - 23070123124
// EXPERIMENT - 20(C)

#include<iostream>
using namespace std;

void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;

        // Move elements of arr[0..i-1], that are greater than key, to one position ahead of their current position
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}

int main() {
    int n;
    cout << "How many elements in your array?" << endl;
    cin >> n;
    
    int arr[n];
    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    insertionSort(arr, n);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    
    return 0;
}
```
## Output:
![image](https://github.com/user-attachments/assets/40f4409f-2352-474e-96d5-2e948db7cd0d)











### Conclusion:
I learnt the study and implement sorting algorithm C++.
