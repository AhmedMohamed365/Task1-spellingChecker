# Task1-spellingChecker
 Spelling Checker to handle correcting words and getting the nearest 4 words

 ## Analysis of complexity : 
1. __init__(self, dictionary):
   - **Time Complexity**: The `__init__` method involves sorting the given `dictionary` list, which takes O(n log n) time, as n is the number of words in the dictionary.
   -** Space Complexity**: The space complexity for sorting is O(n) since we are creating a new sorted list.

2. find_nearest_words(self, word):
   - **Time Complexity**: The `bisect.bisect_left()` function used in the `find_nearest_words()` method has a time complexity of O(log n) for binary search, as n is the number of words in the dictionary. The slicing operation to get the nearest 4 words takes constant time, O(1).
   - **Space Complexity**: The space complexity is O(1) because the method does not create any additional data structures.

3. add_to_dictionary(self, word):
   - **Time Complexity**: The `bisect.bisect_left()` function used in the `add_to_dictionary()` method has a time complexity of O(log n) for binary search, where n is the number of words in the dictionary. Inserting a new word into the sorted list takes O(n) time in the worst case as we may need to shift elements to make space for the new word.
   - Space Complexity: The space complexity is O(1) because the method does not create any additional data structures.

4. print_dictionary(self):
   - **Time Complexity**: The `print_dictionary()` method involves iterating through all the words in the dictionary, which takes O(n) time, as n is the number of words in the dictionary.
   - **Space Complexity**: The space complexity is O(1) because the method does not create any additional data structures.

5. Helper Data Structures:
   - The class uses a sorted list (Python list) to store the dictionary. The space complexity for the sorted list is O(n), as n is the number of words in the dictionary.

In summary, the time complexity of most operations is bounded by the sorting of the dictionary during initialization (O(n log n)), while the other operations  involve binary search (O(log n)) and constant time operations. The overall space complexity is O(n) because of the  sorted list that stores the dictionary.
