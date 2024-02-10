# Delete-and-Balance-Array
You are given an array `a` containing n integer. Your goal is to make this array balanced by removing some elements from the array. You can also rearrange the elements of the array. An array is considered balanced if and only if the absolute difference between any two consecutive elements is at most k. Your task is to delete minimum possible 

def min_deleted_elements(n, arr, k):
    arr.sort()

    deleted_count = 0

    for i in range(1, n):
        if arr[i] - arr[i - 1] > k:
            deleted_count += 1

    return deleted_count

n = int(input())
arr = list(map(int, input().split()))
k = int(input())

result = min_deleted_elements(n, arr, k)
print(result)
