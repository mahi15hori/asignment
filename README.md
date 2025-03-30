#include <iostream>
using namespace std;

template <typename dataType>
void swap(dataType &x, dataType &y) {
    dataType temp = x;
    x = y;
    y = temp;
}

void selectionSort(int dataElement[], int n) {
    using ::swap;
    for (int i = 0; i < n - 1; i++) {
        for (int j = i + 1; j < n; j++) {
            if (dataElement[i] > dataElement[j]) {
                swap(dataElement[i], dataElement[j]);
            }
        }
    }
}

int main() {
    int n;
    cout << "Enter the number of elements: ";
    cin >> n;

    int dataElement[n];
    cout << "Enter " << n << " elements: ";
    for (int i = 0; i < n; ++i) {
        cin >> dataElement[i];
    }

    selectionSort(dataElement, n);

    cout << "Sorted array: ";
    for (int i = 0; i < n; ++i) {
        cout << dataElement[i] << " ";
    }
    cout << endl;
    
    return 0;
}

