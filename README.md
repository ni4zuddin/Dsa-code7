#include <stdio.h>
int linearSearch(int *p, int size, int target) {
    for (int i = 0; i < size; i++) {
        if (*p == target) {
            return i;
        }
        p++;
    }
    return -1;
}
int main() {
    int arr[] = {4, 6, 9, 3, 7, 2};
    int size = sizeof(arr) / sizeof(arr[0]);
    int target;
    printf("Enter no. to search: ");
    scanf("%d", &target);
    int result = linearSearch(arr, size, target);
    if (result != -1) {
        printf("Element %d found at index: %d\n", target, result);
    } else {
        printf("Element %d not found in the array.\n", target);
    }
    return 0;
}
