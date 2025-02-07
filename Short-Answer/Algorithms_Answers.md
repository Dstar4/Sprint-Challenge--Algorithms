Add your answers to the Algorithms exercises here.

a) O(n) - There is one loop which will run (times) directly in proportion to how large n is.

b) O(n^4) - There are 3 for loops that depend on n. The 4th for loop depends on k. Because 4 for loops run in proportion to how large n is. This will have exponential growth.

c) O(n) / O(bunnies) - we call bunnyEars once inside bunnyEars, so that will loop in proportion to how large "bunnies" is



Ex. II

Understand
-------------------
- n story building
- egg is broken if it is thrown off _f_ or higher
- egg doesn't break if thrown off lower than _f_
- determine _f_ such that # of dropped eggs is minimized
- Buildings floors are sequential
- Floors go from 0 to _n_

- We will need an algorithm that gets to _f_ with as few steps possible

- We could use binary search - O(log n) - Since the building floors are sorted lowest -> highest.
- Start at _n_ / 2
- Then select higher or lower if the egg breaks or not and repeat.

Plan
-----------
- We can solve this using binary search since the floors are sorted.

- Drop an egg from _n_ / 2

- If it breaks drop an egg from _n_ / 4 or slice the lower part of _n_/2 and drop from len(new_list) / 2

- If it does not break drop from the midpoint of the upper slice of _n_ / 2

- Continue with this pattern until you get to the floor where the egg breaks but on the floor below it does not. This will == _f_