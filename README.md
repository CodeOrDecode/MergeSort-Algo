# MergeSort-Algo


def getval(arr):
  if len(arr) == 1:
    return arr
  
  elif len(arr)>1:
    mid = len(arr)//2
    leftp = arr[:mid]
    rightp = arr[mid:]
    left = getval(leftp)
    right = getval(rightp)
    i = 0 
    j = 0 
    k= 0 
    while i< len(left) and j<len(right):
      if left[i]<right[j]:
        arr[k] = left[i]
        i = i+1 
        k = k+1 
        
      else:
        arr[k] = right[j]
        j = j+1 
        k = k+1
        
    while i< len(left):
      arr[k] = left[i]
      i = i+1 
      k = k+1 
      
    while j< len(right):
      arr[k] = right[j]
      j = j+1 
      k = k+1 
      
    return arr


arr=[10,9,8,7,6]
getval(arr)
print(arr)
