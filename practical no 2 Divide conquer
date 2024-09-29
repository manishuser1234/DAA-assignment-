def find_max_min(arr, low, high):
    # If the array contains only one element
    if low == high:
        return arr[low], arr[low]
    
    # If the array contains two elements
    elif high == low + 1:
        if arr[low] > arr[high]:
            return arr[low], arr[high]
        else:
            return arr[high], arr[low]
    
    # If the array contains more than two elements, divide the array into two halves
    else:
        mid = (low + high) // 2
        max1, min1 = find_max_min(arr, low, mid)
        max2, min2 = find_max_min(arr, mid + 1, high)
        
        # Combine the results of the two halves
        return max(max1, max2), min(min1, min2)

# Example usage
arr = [100, 5, 20, 15, 78, 45, 10, 95]
n = len(arr)

max_val, min_val = find_max_min(arr, 0, n - 1)
print(f"Maximum element: {max_val}")
print(f"Minimum element: {min_val}")
