
# Day 4 – #28DaysOfTesting

![Day 4 – Validation Failure](../Resources/Day_4.png)

I cleared the quantity field, clicked the `+` icon, and the cart total became `NaN`.

What stood out was that the system didn’t stop there.  
Checkout still succeeded.

This isn’t a UI glitch.  
It’s a validation failure where an invalid monetary state is allowed to pass through the entire flow.

Testing isn’t just about finding bugs.  
It’s about asking one important question:

**What should never be allowed to happen?**

🔗 Potion Shop:  
https://epictestquest.github.io/the-Potion-Shop/