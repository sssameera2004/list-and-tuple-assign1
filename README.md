def last(n):
    return n[-1] 
  
def sort(tuples):
    return sorted(tuples, key=last)
  
a=[(1, 3), (3, 2), (2, 1)]
print("Sorted:")
print(sort(a))
OUTPUT:-[(2,1),(3,2),(1,3)]

METHOD2:-
def Sort_Tuple(tup): 
       
    # getting length of list of tuples
    lst = len(tup) 
    for i in range(0, lst): 
           
        for j in range(0, lst-i-1): 
            if (tup[j][-1] > tup[j + 1][-1]): 
                temp = tup[j] 
                tup[j]= tup[j + 1] 
                tup[j + 1]= temp 
    return tup 
 # Driver Code 
tup =[(1, 3), (3, 2), (2, 1)]
 print(Sort_Tuple(tup))
OUTPUT:-[(2,1),(3,2),(1,3)]

Method3:-
def Sort_Tuple(tup): 
   
    # reverse = None (Sorts in Ascending order) 
    # key is set to sort using second element of 
    # sublist lambda has been used 
    tup.sort(key = lambda x: x[-1]) 
    return tup 
   
# Driver Code 
tup = [(1, 3), (3, 2), (2, 1)]
   
# printing the sorted list of tuples
print(Sort_Tuple(tup)) 
OUTPUT:-[(2,1),(3,2),(1,3)]
