# Math 187A - Quiz 1 Corrections

## Problem 9

Q: In year N-1, the 200th day of the calendar year is a Monday. In year N, the 100th day of the calendar year is again a Monday. On what day of the week will the very last day of calendar year N+1 fall? Explain.

### A) (correct solution)

~~> Assuming years N-1, N, and N+1 are NOT leap years.~~

Let n = days since year N-1 started 
- (including the first day - i.e. n = 1 corresponds to day 1 of year N-1

```
KEY DATES (assuming no leap years)
-------------------------------------------
n = 1               : 1st   day of year N-1
n = 200             : 200th day of year N-1
n = 365             : last  day of year N-1
n = 365+1 = 366     : 1st   day of year N
n = 365+100 = 465   : 100th day of year N
n = 365+365 = 730   : last  day of year N
n = 730+1 = 731     : 1st   day of year N+1
n = 730+365 = 1095  : last  day of year N+1
```

Each n can be represented as 

$$ n = 7w + d $$

Where:
- w: represents weeks passed since N-1 started (w = 0 for n=0 through n=6)
- d: day of the week (will discover correspondance later)

We know that it is Monday for `n=200` and `n=465`

$$ 200 = 7(28) + 4\\
   465 = 7(66) + 3$$

Here we find out that the assumption of no leap years was incorrect. In order for (200th day of year N-1) and (100th day of year N) to land on the same `d` (day of the week), their respective values would've had to be `n=200` and `n=466`; In order for this to be true, then year N-1 must've been a leap year and the KEY DATES chart would've had to be re-arranged as so:

```
KEY DATES (N-1 is a leap year)
-------------------------------------------
n = 1               : 1st   day of year N-1
n = 200             : 200th day of year N-1
n = 366             : last  day of year N-1
n = 366+1 = 367     : 1st   day of year N
n = 366+100 = 466   : 100th day of year N
n = 366+365 = 731   : last  day of year N
n = 731+1 = 732     : 1st   day of year N+1
n = 731+365 = 1096  : last  day of year N+1
```

Now, the given statements match up:

$$ 200 = 7(28) + 4\\
   466 = 7(66) + 4$$

We now know that the (200th day of year N-1) and (100th day of year N) occurred on the 4th day of the week, which was given to be a Monday. This lets us generate this day of week chart:

```
Day of Week
---
d = 4 : Monday
d = 5 : Tuesday
d = 6 : Wednesday
d = 0 : Thursday
d = 1 : Friday
d = 2 : Saturday
d = 3 : Sunday
```

Finally, we were tasked with finding the day of week that the last day of year N+1 (`n=1096`) would fall on:

$$ 1096 = 7(156) + 4$$

This tells us that the last day of year N+1 would also fall on the 4th day of the week, which we know corresponds with Monday.

Final answer: The last day of year N+1 would fall on a **Monday**

### B) (What was wrong with solution on quiz / misunderstood key concepts)

1. Assumed no leap years
2. Miscalculated values of `n` in my original work, which masked the misallignment that would've revealed the inability to assume no leap years
3. A bunch of arithmetic + logic errors
    - Stated `n=366` corresponded with (day 1 of year N) and `n=466` corresponded with (day 100 of year N) 
    > which is a contradiction: `366` and `465` would correspond or `367` and `466` would correspond
    - Stated `n=731` corresponded with (day 1 of year N+1) and `n=995` corresponded with (last day of year N) 
    > must've mean to add 364 to 731 but accidentally added 264 to 731

### C) Resources used

- VSCode to write this markdown file (cleaner + faster than handwriting)
- Calculator (HP Portable Prime -- resorted to a Graphing Calc since I seemed to have misplaced my TI-86X pro)
- Time (I rushed through the quiz on Friday to go to the bathroom)