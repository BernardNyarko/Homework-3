# Homework-3         ML functions and Patterns
- Student:             Bernard Nyarko;   ID: P22188665
- Lecturer:            Professor(Associate) Ahmed Abdelmoamen Ahmed
- Course:              Fundamentals and Concepts of Programming Languages
- Turn in Date:        11/08/2020
- Homework 3 Solutions

(1) - fun Cuber (x: real): real = x * x * x;
    - Cuber 3.0;
The function Cuber takes an input number (x) and converts it to a real (float) number.
": real " which comes after "(x: real)" makes show that the output of the function is a real (float) number.
The function works by multiplying the input number three (3) times and returns the output. In this case the 
function takes an input value of 3.0 and the return output is:
- val Cuber = fn : real -> real
val it = 27.0 : real

(2) - fun fourth (x) = hd (tl (tl (tl x)));
     - fourth [1, 2, 34, 5, 6];
The function fourth takes an input list (x) and finds the fourth (4) number in the input list as the out put
and returns it. Using key words hd (head) and tl (tail) in ML to manipulate the list, the fourth value of the
list is retrieved. In this case the function takes an input list of [1, 2, 34, 5, 6]; and the return output is:
- val fourth = fn : 'a list -> 'a
val it = 5 : int

(3) - fun min3 (x, y, z) =
     - if x < y andalso x < z
     - then x
     - else if y < x andalso y < z
     - then y
     - else z;
     - min3 (5,9,0);
The function min3 takes an input of three integers in a tuple and finds the minimum of the three integers 
using if, else if, and else key words in ML to provide a series of condition statements. When a condition is met, 
the function returns an output that the condition specifies. In this case the function takes an input value of 
(5,9,0) and the return ouput is:
- val min3 = fn : int * int * int -> int
val it = 0 : int

(4) - fun Cycle1(x) =
     - if null x 
     - then x
     - else tl (x) @ [ hd (x) ];
     - cycle1 [1, 2, 3, 4, 5, 6, 7];
The function Cycle1 takes an input list (x) and returns the input list as the outout but with the first element of
the input list move to the end of the output list. if the input list is null (empty), it returns a null list. If 
the input list is not null, the tail (all elements apart from the first element) of the input list is retrieved 
first after which it is concatenated with the head (first element) of the input list. Using if, and else 
key words in ML to provide a series of condition statements, when a condition is met, the function returns an 
output that the condition specifies. In this case the function takes an input list of [1, 2, 3, 4, 5, 6, 7] and the
return ouput is: 
- val cycle1 = fn : 'a list -> 'a list
val it = [2,3,4,5,6,7,1] : int list

(5) - fun sqsum x =
      - if x = 0 then 0
      - else (x * x) + sqsum (x - 1);
      - sqsum 4;
The function sqsum takes a positive input integer (x) and returns the sum of the squares of all the integers zero (0)
through 'x' using if, and else in a series of conditions. When a condition is met, the function returns an 
output that the condition specifies. In this case the function takes an input value of 4 and the return output is: 
- val sqsum = fn : int -> int
val it = 30 : int

(6) - fun member (e, [ ])= false | member (e, x :: xs) = if (e = x)
      - then true
      - else member(e, xs);
      - member (1, [ ]);
      - member (8, [7, 8]);
The function member takes an input tuple of two elements of which the second is a list and returns either true or false 
when the first element in the tuple is found in the second element (list) in the tuple using if, and else condition 
statements. In this case the function takes input values of (1, [ ]) and (8, [7, 8]). The return output are: 
- val member = fn : ''a * ''a list -> bool
val it = false : bool
val it = true : bool

(7) - fun less (e, [ ]) = [ ] | less (e, x :: xs) = 
      - if x < e 
      - then x :: less (e, xs) 
      - else less (e, xs);
      - less(10, [3, 4, 5, 0, 7, 8, 50]);
The function 
