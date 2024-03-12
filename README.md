# -java-binary-search
# Binary Search Algorithm in Java
# 1.Start
# 2.Take input array and Target
# 3.Initialise start = 0 and end = (array size -1)
# 4.Intialise mid variable
# 5.mid = (start+end)/2
# 6.if array[ mid ] == target then return mid
# 7.if array[ mid ] < target then start = mid+1
# 8.if array[ mid ] > target then end = mid-1
# 9.if start<=end then goto step 5
# 10.return -1 as Not element found Exit
# approach1
public int binarySearch(int[] arr, int x) {
    int left = 0;
    int right = arr.length - 1;

    while (left <= right) {
        int mid = left + (right - left) / 2;

        if (arr[mid] == x) {
            return mid;
        }

        if (arr[mid] < x) {
            left = mid + 1;
        } else {
            right = mid - 1;
        }
    }

    return -1; // element not found
}

# approach2
# Python3 code to implement iterative Binary
# Search.


# It returns location of x in given array arr
def binarySearch(arr, l, r, x):

	while l <= r:

		mid = l + (r - l) // 2

		# Check if x is present at mid
		if arr[mid] == x:
			return mid

		# If x is greater, ignore left half
		elif arr[mid] < x:
			l = mid + 1

		# If x is smaller, ignore right half
		else:
			r = mid - 1

	# If we reach here, then the element
	# was not present
	return -1


# Driver Code
if __name__ == '__main__':
	arr = [2, 3, 4, 10, 40]
	x = 10

	# Function call
	result = binarySearch(arr, 0, len(arr)-1, x)
	if result != -1:
		print("Element is present at index", result)
	else:
		print("Element is not present in array")
# o/p:Element is present at index 3

