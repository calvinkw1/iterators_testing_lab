##Descriptions of Iterators

###Instructions
Below you will find a list of methods. In the space provided below each, please provide a brief description of what this method does based upon your review of the Docs. 

###Array methods:
May be helpful to look in [Enumerable](http://ruby-doc.org/core-2.2.0/Enumerable.html) as well...

####select:
Returns an array of the enumerators or, items in an array, that evaluate to TRUE via the conditions specified in the code block. Opposite of "reject".

####reject:
Returns an array of the enumerators or, items in an array, that evaluate to FALSE via the conditions specified in the code block. Opposite of "select".

####map:
Creates a copy of an array but with the elements modified via the conditions in the code block.

####detect:
Returns the first truthy element of an array that is passed to the code block. Returns nil if no match found.

####inject:
Combines all elements of an array by way of a code block or a symbol that represents a method/operator. Takes in 2 parameters (accumulator, element) and returns the accumulator at the end of the iteration.

####partition:
Returns 2 arrays, 1 of which contains all elements that evaluated truthy based on the specified code block. The other array contains the falsey or remainder elements.
(Ruby docs doesn't mention that the 2 arrays are returned inside another array)

####sort:
Returns an array of sorted elements either according to the default sorting method or by what's specified in the code block. The block returns -1, 0, 1, based on the comparison between the 1st and 2nd parameters, using the <=> comparison.

####one?:
Returns "true" only if the array only has one "truthy" element based on the code block conditions. This is also the default if no code block is specified.

####none?:
Returns "true" only if the array elements have no "truthy" elements based on the code block conditions. This is also the default if no code block is specified.

####all?:
Will return "true" if the array elements passed to the code block never return "false" or "nil". If no block given, Ruby will auto-add a block of "{|obj| obj}" which will default to "true"

####empty?:
Will return true if array/string has a length of 0, or in essence, is empty.

####eql?:
Equivalent of using "==" but with the caveat of not working for number comparisons. Returns a boolean value based on the equality.

####include?:
Returns true as long as the parameter specified exists inside the array. If it doesn't, returns false.

####nil?:
Will only return true if the object is nil.

###Hash methods:

####key?:
Will return true if the given key exists inside the hash.

####keys:
Returns a new array with all of the keys that exist inside the hash.

####delete:
Deletes the specified object from the hash and returns that object. Returns nil if the specified object does not exist in hash. Optional code block is also returned if object does not appear in the hash, which can be used as an error message that you specify.

####delete_if:
Used to delete items from the hash through a given condition that evaluates the item to be true. Each deletion affects the hash immediately instead of when the iteration is complete.
