
**Pointer Cheatsheet**
--

- A pointer must always be of the same type as the variable it's pointing at. 
- Declaring a pointer variable does not create the type of variable it points at. It creates a pointer variable.
- Though pointers are declared with an asterisk they are not always used with an asterisk.   
- The asterisk is the unary * operator. It is not the * multiplication operator.   
- Pointers must be initialized before they can be used.   
- Initialize a pointer by assigning it to a variable; the variable must be of the same type as the pointer.
- To assign a pointer to a variable, use an ampersand with the variable's name. 
- The address-of unary operator & is not the same as the bitwise & AND operator.
---
	m_address = &memory;

  To assign a pointer to an array, do not use the ampersand:

      s_address = string;

  The pointer s_address would be used on the string array's elements.
  To assign a pointer to an array element, use the ampersand:
  
    element = &string[2];

  Without an asterisk, an initialized pointer holds a memory address.
  With an asterisk, an initialized pointer references the value stored at its address.

**Typical Pointer Setup and Use**

First, create a pointer of the proper type:

    float *f;

Second assign it to a variable's memory location:

    f = &boat;

Finally, use the pointer:

    printf("%.0f",*f);

Without an asterisk, the pointer references a memory location.
With an asterisk, the pointer references the value at that memory location.
Always use the same type of pointer as the variables it examines: floats for floats, ints for ints, and so on.
Remember: initialize a pointer before you use it! Set the pointer equal to the address of some variable in memory.


**Pointers, Parenthesis and Math**
--
| Pointer Thing        | Memory Address                        |Memory Contents
|----------------------|---------------------------------------|--------------------
| p                    | Yep                                   | Nope
| *p                   | Nope                                  | Yep
| *p++                 | Incremented after value is read       | Unchanged
| *(p++)               | Incremented after value is read       | Unchanged
| (*p)++               | Unchanged                             | Incremented after it's used
| *++p                 | Incremented before value is read      | Unchanged
| *(++p)               | Incremented before value is read      | Unchanged
| ++*p                 | Unchanged                             | Incremented before it's used
| ++(*p)               | Unchanged                             | Incremented before it's used
| p*++                 | Not a pointer                         | Not a pointer
| p++*                 | Not a pointer                         | Not a pointer

The ++ operator is used above, though any math operation can be substituted.

*A tip: Use parenthesis to isolate part of the pointer problem and the answer will always work out the way you intended.*

**Pointers and array brackets**
--
| Array Notation | Pointer Equivalent  
|----------------|---------------------
| array[0]   	 | *a		
| array[1]  	 | *(a+1)  	
| array[2]   	 | *(a+2)  	
| array[3]     | *(a+3) 		
| array[x]  	 | *(a+x)     	

**Ugly ** notation**

| Doodad             | What It Is                              | Seen by The Compiler
|--------------------|-----------------------------------------|---------------------
| array+1            | An address                              | A pointer
| *(array+1)         | Contents of address, what lives there   | A string
| \*(*(array+1))     | Contents of a character array           | A character
| **(array+1)        | Same as above                           | Same as above

[Pointer Cheetsheet by Dan Gookin .](https://www.c-for-dummies.com/caio/pointer-cheatsheet.php)
