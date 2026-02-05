```md
# Day 5 of #28DaysOfTesting

There’s a weird shame around running **“extra” tests**.

Like you should somehow stick to the scope.  
Test what changed.  
Don’t waste time on things that probably still work.

> “That’s out of scope.”  
> “It wasn’t in the ticket.”  
> “You’re overthinking it.”

I’ve heard all of these.  
From other testers.  
From myself.

And yet.

I was testing a **sorting algorithm change**.  
Wrote my test. It passed. Done.

But I thought, *“Let me just run this on the other lists too.”*  
No reason. Just curiosity.

The new sorting hid every item with a **0 count**.  
Users couldn’t see things they didn’t own yet.  
Couldn’t select them.

The entire point of that page—**invisible**.

That “out of scope” test saved the release.

---

💭 **Your turn:**  
Share a test you almost didn’t write because it felt unnecessary, out of scope, or too paranoid.  
What did it catch?

I think we need to stop treating **curiosity** as a waste of time.  
If something in your gut says *“check this too,”* that’s probably your experience talking.

Listen to it.
```

# My Story


```md
## An Out-of-Scope Test That Mattered

While testing new features in a product that was already live, I decided—out of pure curiosity—to open the **Profile** tab and change the profile picture.

I uploaded a **GIF**.  
The app crashed.

Uploading GIFs wasn’t blocked, and this scenario wasn’t part of my test scope.  
But it was a very real user action.

That single “out of scope” check exposed a crash that would have gone to production  
if I had stuck strictly to the ticket.
```
