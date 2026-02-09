```md
# Day 9 of #28DaysOfTesting

Week 2 starts now.

What is the fastest you have ever found a **critical bug**  
From starting to test to that sudden moment of oh no  
How long did it take

Mine was about two minutes.

It was a date picker on a registration form.  
It opened fine.  
It looked fine.  
It let me select a date.

I hit submit.

The backend received null.

The entire form was silently broken.  
The user interface looked perfect, but the data simply vanished.

I found it because I actually completed the form instead of only checking whether it rendered correctly and allowed selection.

Later, we found that the date picker library had been updated.  
All tests were green, but my gut feeling was off.

What is the fastest critical bug you have ever found
```

![Day 9 - What is the fastest critical bug you have ever found?](../Resources/day_9.png)
