---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is a numbered list of objects. The objects of an array can be of any class, including arrays themselves. 

# What are some examples of information that would be Arrays as opposed to some other data type?

A grocery list, the names of candidates in an election, the ingredients in a recipe, and a list of favorite movies could all be stored as arrays. 

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

If you have an array `favorite_bands`, the line `puts favorite_bands[5]` would retrieve the 6th element in an array, `puts favorite_bands[7]` would retrieve the 8th, and so on. If you try to retrieve the value of an element that doesn't exist, the output will be 'nil'.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Yes. To find the -6th element (The 6th-to-last element in the array) in `favorite_bands`, you can use `puts favorite_bands[-6]`.

# How would you perform an operation on every element inside an Array?

You would use the `each` method, by writing `array_name.each do |element|`, followed by the operation you want to perform on each `element`.

# How do you add elements to an Array?

By assigning an object to an element that previously had none. So, if `puts array[6]` would return `nil`, then `array[6] = 'new element'` adds the string `'new element'` as the 7th (new) element of the array.

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

If the name of the array is `my_friends`, then `my_friends[1] = "Florence"` would replace `"Fiona"` (or whatever else `my_friends[1]` was assigned to) with `"Florence"`, without changing any of the other elements' assignments.

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

`push` adds an element to the end of the array, `pop` retrieves and removes the last object in the array, `shift` retrieves and removes the *first* object in the array, and `unshift` adds an element to the front of the array, pushing the rest of the objects back one slot.

# How do you determine how many elements are in an Array?

By using `myarray.length`, `myarray.count`, or `myarray.size`. `length` and `size` are interchangeable; `count` has functions beyond this, but can be used for this purpose.

# How would you reverse the order of elements in an Array?

By using the `reverse` operation.

Note: I spent probably an hour trying to figure out a longer way to do it on my own, and the best answer I had before googling it was by defining a new array, `arynew = []`, and performing the following code:
array.each do |element|
    arynew.unshift(element)
end

array = arynew

Needless to say, the ruby-doc.org website could be a little more user-friendly.

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

`"Sumeet Jain".split` will split a string into an array of all the words (or, more specifically, sequences of characters that aren't spaces) in the string, and `"Sumeet Jain".chars` will return an array all the characters in the string. Adding `to_s` to the end of the array would convert it back into a string.