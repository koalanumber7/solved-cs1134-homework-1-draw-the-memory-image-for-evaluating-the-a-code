Download Link: https://assignmentchef.com/product/solved-cs1134-homework-1-draw-the-memory-image-for-evaluating-the-a-code
<br>
<strong><u>Question 1</u></strong><u>:</u>

Draw the memory image for evaluating the following code: &gt; &gt; &gt; lst1 = [1, 2, 3]

&gt;&gt;&gt; lst2 = [lst1 <strong>for </strong>i <strong>in </strong>range(3)]

&gt;&gt;&gt; lst2[0][0] = 10

&gt;&gt;&gt; print(lst2)

<strong><u>Question 2 </u></strong> :

<ol>

 <li>Write a function <strong>def </strong>shift(lst, k) that is given a list of <em>N </em>numbers, and some positive integer k (where k<em>&lt;N</em>). The function should shift the numbers circularly k steps to the left.</li>

</ol>

The shift has to b e done <strong>in-place</strong>. That is, the numbers in the parameter list should reorder to form the correct output (you <strong>shouldn’t </strong>create and return a new list with the shifted result).

For example, if lst = [1, 2, 3, 4, 5, 6] after calling shift(lst, 2), l s t will b e [3, 4, 5, 6, 1, 2 ]

b . Modify your implementation, so we could optionally pass to the function a third argument that indicates the direction of the shift (either ‘left’ or ‘right’).

<u>Note:</u> if only two parameters are passed, the function should shift, by default, to the left.

<u>Hint:</u> Use the syntax for default parameter values.

<strong><u>Question 3 </u></strong> :

<ol>

 <li>Write a short Python function that takes a positive integer <em>n </em>and returns the sum of the squares of all the positive integers smaller than <em>n</em>.</li>

</ol>

b . Give a single command that computes the sum from section (a), relying on Python’s list comprehension syntax and the built-in sum function.

<ol>

 <li>Write a short Python function that takes a positive integer <em>n </em>and returns the sum of the squares of all the odd positive integers smaller than <em>n</em>.</li>

 <li>Give a single command that computes the sum from section (c), relying on Python’s list comprehension syntax and the built-in sum</li>

</ol>




<strong><u>Question 4</u></strong> :

<ol>

 <li>Demonstrate how to use Python’s list comprehension syntax to produce the list [1, 10, 100, 1000, 10000, 100000] .</li>

</ol>

b . Demonstrate how to use Python’s list comprehension syntax to produce the list [0, 2, 6, 12, 20, 30, 42, 56, 72, 90].

<ol>

 <li>Demonstrate how to use Python’s list comprehension syntax to produce the list[‘a’, ‘b’, ‘c’, … , ‘z’] , but without having to type all 26 such characters literally.</li>

</ol>

<strong><u>Question 5: </u></strong>

The <em>Fibonacci Numbers Sequence</em>, <em>F<sub>n</sub></em>, is defined as follows:

<em>F</em><em>0 </em>is <em>1</em>, <em>F</em><em>1 </em>i s <em>1</em>, and <em>F<sub>n</sub> = F</em><em>n-1 </em><em>+ F</em><em>n-2 </em>for <em>n = 2, 3, 4, …</em>

In other words, each number is the sum of the previous two numbers.

The first 10 numbers in Fibonacci sequence are: 1, 1, 2, 3, 5, 8, 13, 21, 34, 55

<u>Note:</u>

Background of Fibonacci sequence: <u><a href="https://en.wikipedia.org/wiki/Fibonacci">https://en.wikipedia.org/wiki/Fibonacci</a></u><u> number</u>

Implement a function <strong>def </strong>fibs (n). This function is given a positive integer n, and returns a <u>generator,</u> that when iterated over, it will have the first n elements in the Fibonacci sequence.

For Example, if we execute the following code: <strong>for </strong>curr <strong>in </strong>fibs(8):

print(curr)

The expected output is:

1 1 2 3 5 8 13 21




<strong><u>Question 6</u></strong><u>:</u>

You are given an implementation of a Vector class, representing the coordinates of a vector in a multidimensional space. For example, in a three-dimensional space, we might wish to represent a vector with coordinates <em>&lt;5,</em><em>−</em><em>2, 3&gt;</em>.

For a detailed explanation of this implementation as well as of the syntax of operator overloading that is used here, please read sections 2.3.2 and 2.3.3 in the textbook (pages 74-78).

<strong>class </strong>Vector:

<strong>def </strong>__init__ (self, d): self.coords = [0]*d

<strong>def </strong>__len (self):

<strong>return </strong>len(self. coords)

<strong>def </strong>__ getitem__ (self, j): <strong>return </strong>self.coords[j]

<strong>def </strong>__ setitem__ (self, j, val):self.coords[j] = val

<strong>def </strong>__add (self, other):

<strong>if </strong>(len(self) != len(other)):

<strong>raise </strong>ValueError(”dimensions must agree”) result = Vector(len(self))

<strong>for </strong>j <strong>in </strong>range(len(self)):

result[j] = self[j] + other[j]

<strong>return </strong>result

<strong>def </strong>__eq (self, other):

<strong>return </strong>self.coords == other.coords

<strong>def </strong>__ne (self, other):

<strong>return not </strong>(self == other)

<strong>def </strong>__str (self):

<strong>return </strong>’&lt;’+ str(self.coords)[1:−1] + ’&gt;’

<strong>def </strong>__repr (self): <strong>return </strong>str(self)




<ol>

 <li>The Vector class provides a constructor that takes an integer <em>d</em>, and produces a <em>d</em>-dimensional vector with all coordinates equal to 0. Another convenient form for creating a new vector would be to send the constructor a parameter that is some iterable object representing a sequence of numbers, and to create a vector with dimension equal to the length of that sequence and coordinates equal to the sequence values. For example, Vector([4, 7, 5]) would produce a three-dimensional vector with coordinates <em>&lt;4, 7, 5&gt;</em>.</li>

</ol>

Modify the constructor so that either of these forms is acceptable; that is, if a single integer is sent, it produces a vector of that dimension with all zeros, but if a sequence of numbers is provided, it produces a vector with coordinates based on that sequence.

<u>Hint:</u> use run-time type checking (the isinstance function) to support both syntaxes.

b . Implement the __sub__ method for the Vector class, so that the expression <em>u</em><em>−</em><em>v </em>returns a new vector instance representing the difference between two vectors.

<ol>

 <li>Implement the __neg__ method for the Vector class, so that the expression <em>−</em><em>v </em>returns a new vector instance whose coordinates are all the negated values of the respective coordinates of <em>v</em>.</li>

 <li>Implement the __mul__ method for the Vector class, so that the expression <em>v*3 </em>returns a new vector with coordinates that are <em>3 </em>times the respective coordinates of <em>v</em>.</li>

</ol>

e . Section (d) asks for an implementation of __mul__ , for the Vector class, to provide support for the syntax <em>v *3</em>.

Implement the __rmul__ method, to provide additional support for syntax <em>3 *v</em>.

<ol>

 <li>There two kinds of multiplication related to vectors:</li>

</ol>

1 . Scalar product – multiplying a vector by a number (a scalar), as described and implemented in section (d) .

For example, if <em>v = &lt;1, 2, 3&gt;</em>, then <em>v*5 </em>would be <em>&lt;5, 10, 15&gt;</em>.

2 . Dot product – multiplying a vector by another vector. In this kind of multiplication if <em>v = &lt;v</em><em>1</em><em>, v</em><em>2</em><em>, É, v<sub>n</sub>&gt; </em>and <em>u = &lt;u</em><em>1</em><em>, u</em><em>2</em><em>, É, u<sub>n</sub>&gt; </em>then <em>v*u </em>would be

<em>v</em><em>1</em><em>*u</em><em>1 </em><em>+ v</em><em>2</em><em>*u</em><em>2 </em><em>+ É + v </em><em>n</em><em>*u</em><em>n</em>.

For example, if <em>v = &lt;1, 2, 3&gt; </em>and <em>u = &lt;4, 5, 6&gt;</em>, then <em>v*u </em>would be 3 2 ( 1 *4 + 2 * 5 + 3 * 6 = 3 2 ).

Modify your implementation of the __mul__ method so it will support both




kinds of multiplication. That is, when the user will multiply a vector by a number it will calculate the scalar product and when the user multiplies a vector by another vector, their dot product will be calculated.

After implementing sections (a)-(f), you should expect the following behavior:

&gt; &gt; &gt; v1 = Vector(5)

&gt;&gt;&gt; v1[1] = 10

&gt;&gt;&gt; v1[−1] = 10 &gt;&gt;&gt; print(v1)

&lt;0, 10, 0, 0, 10&gt;

&gt;&gt;&gt; v2 = Vector([2, 4, 6, 8, 10]) &gt;&gt;&gt; print(v2)

&lt;2, 4, 6, 8, 10&gt;

&gt;&gt;&gt; u1 = v1 + v2 &gt;&gt;&gt; print(u1)

&lt;2, 14, 6, 8, 20&gt;

&gt;&gt;&gt; u2 = -v2

&gt;&gt;&gt; print(u2)

&lt;-2, -4, -6, -8, -10&gt;

&gt;&gt;&gt; u3 = 3 * v2

&gt;&gt;&gt; print(u3)

&lt;6, 12, 18, 24, 30&gt;

&gt;&gt;&gt; u4 = v2 * 3

&gt;&gt;&gt; print(u4)

&lt;6, 12, 18, 24, 30&gt;

&gt;&gt;&gt; u5 = v1 * v2 &gt;&gt;&gt; print(u5)

140