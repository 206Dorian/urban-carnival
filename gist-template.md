# Urban Carnival

My First RegEx Article About Coding.

In this gist I will dive into the exciting world of a regex! 
A regex is a sequence of characters that defines a specific search pattern.   This search pattern will allow a user to search through a group of characters like a document or a group of code and find the characters that match the specified parameters.

Does that clear it all up??  Of course not, those were all just words in a sentence that I could recognize, but didn't fully comprehend  (much like a regex sequence) until I dug a little deeper. 

I'm a very visual learner and in the abstract world of coding it's hard for me to connect an idea until I can see it on paper being spelled out, so being able to look at this and dissect it really helped and I hope it helps you too. 

Let's look at an example and the components that allow it to function. 


## Summary

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

This is a hex value, it is a positional numbering system that allows us to represent large numbers in a more concise way than traditional binary numbering.  This allows for users to distinguish the numbers more easily as we will use a string of numbers and letters. 


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [OR Operator](#or-operator)


## Regex Components

### Anchors
`“^”` is an anchor which signifies this is the beginning of the statement or line of text/code.   It means that the expression we are looking to match will begin with the following character `“#”` this is a very common way to start a hex value when the value is meant to represent a color.

We also have the ending anchor.
The search is wrapped in the closing parenthesis and then followed by a dollar sign `“$”` 
The `“$”` means this is the end of the statement and it is how we close a regex search.   That's an easy one, you're welcome. 

 If we wanted to search for a specific hex value, we could limit the characters we ask the regex to search for but this is used to search for hex values in general and can be tailored by the user for their purposes.


### Quantifiers
Often a hex value will begin with a hash. However, it’s not required in all cases that the hex value begins with the hash symbol.  So the question mark symbol `“?”` follows the hash.  The question mark character “?” makes the preceding character optional within the search.

### Grouping and Capturing

The second part of the hex value expression is wrapped in parenthesis “()”.  We in coding are VERY familiar with parenthesis. 
Everything contained inside these parentheses are interpreted as a group of characters and not handled individually.  In this case it is the end of the expression.

### Bracket Expressions
Square brackets, or bracket expressions, This is a bog one kids, buckel up!  
`“[]”` match any single character from within the bracketed list.
 For  `[a-f0-9]` it means that our search will find any string that contains “a,b,c,d,e,f” and “0,1,2,3,4,5,6,7,8,9”   Because the characters are being separated by the hyphen which is not read as a character but is a part of the bracket expression syntax. 
 
  Immediately following the square brackets we have curly braces `“{}”` with a number inside `{6}`.  This part of the expression is meant to limit the quantity of characters in the search.  So, since we are looking for characters a-f and 0-9 we are also limiting the search to match a string of 6 characters.  


### OR Operator
 The Bar character `“|”` or  “or” meaning that the search can match the previous parameters OR the following parameters.  In this  regex we have a repetition of the characters included from our previous section `[a-f0-9]` but this time the quantity limiter is listed as 3 characters by using `“{3}”`.



## Author
Dorian Birch

I hope this made you smile and understand regex a little better, here is my github if you want to see any other repos or have any questions for me, feel free to email me as well 206dorian@gmail.com

https://github.com/206Dorian



