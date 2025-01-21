bubble sort : #include <iostream>
using namespace std;

int main() {
    int n;

    // Ask the user for the size of the array
    cout << "Enter the number of elements: ";
    cin >> n;

    int a[n];

    // Input the array elements
    cout << "Enter " << n << " elements: ";
    for (int i = 0; i < n; i++) {
        cin >> a[i];
    }

    // Bubble sort algorithm
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - 1 - i; j++) {
            if (a[j] > a[j + 1]) {
                // Swap elements
                int temp = a[j];
                a[j] = a[j + 1];
                a[j + 1] = temp;
            }
        }
    }

    // Print the sorted array
    cout << "Sorted Array: ";
    for (int i = 0; i < n; i++) {
        cout << a[i] << " ";
    }
    cout << endl;

    return 0;
}
