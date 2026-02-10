```md
# Day 10 of #28DaysOfTesting

I want a number from you today.

Pick any feature. Something from your current project, or the Potion Shop site from Day 3 (link in the comments).

Set a timer. Write two solid test cases from scratch. Or test charters. Or Gherkin scenarios. Use whatever format you actually use at work. The kind you would submit with confidence, not rough notes you would feel the need to clean up later.

Start the timer when you start thinking.  
Stop when you are done.

Share your number and the format you went with.

---

## My Attempt

Today’s challenge was about time.

So we have to pick a feature, start the timer, and write two solid test cases in the format you actually use at work. No overthinking. No polishing later.

**My number:** 1 minute 58 seconds  
**Format:** Gherkin

### Test Case 1 - Elixir of Eternal Focus is successfully added to the cart
**Given** the user is on the homepage  
**When** the user clicks on the Add to Order call to action  
**Then** the Elixir of Eternal Focus should be added to the cart

### Test Case 2 - Correct gold amount is displayed in the cart
**Given** the Elixir of Eternal Focus is added to the cart  
**When** the user navigates to the cart  
**Then** the correct gold amount is displayed in the cart

The takeaway for me was not speed for the sake of speed, but clarity under time pressure. Even in under two minutes, it is possible to write test cases that are clear, complete, and something I would actually submit.


```
