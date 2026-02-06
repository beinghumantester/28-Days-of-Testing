# Day 6 – #28DaysOfTesting

Yesterday was about curiosity saving releases.  
The extra test.  
The gut check.  
Trusting your instincts.

Today is about what happens **after** there are no more tests to run.

The release is out.  
The pipeline is green.  
Your test cases have passed.

And yet… you still can’t close your laptop.

You’re scanning logs.  
Refreshing dashboards.  
Maybe even checking production in your pyjamas before breakfast  
(thanks Sara Åkerlindh for sharing that feeling).

That post-release anxiety?  
It never fully goes away.  
Not after 2 years.  
Not after 18.

---

## Day 6 Challenge

Describe a time when you shipped something and had that  
**“What did I miss?”** feeling.

What happened next?  
- A bug in production?  
- Or worry for nothing?

---

## My Story

In one of my earlier projects, we used to create backward compatibility (grandfathering) test cases for every release. Some were generic, while others were specific to the sprint features. The idea was to leave the application in different states before deployment and, after deployment, take those states to a terminal state to ensure everything still worked as expected.

During one particular release, I missed a basic step—I didn’t verify the build number before setting up the backward compatibility scenarios. Later, when I asked DevOps to deploy the latest build, I was told it had already been deployed at someone else’s request. Rolling back to the previous build wasn’t simple; it required taking a snapshot from the production build and redeploying, which was time-consuming.

Given the situation, we decided to skip the grandfathering cases and proceed with sanity testing. Sanity passed, but the anxiety didn’t. For days, there was this constant *“what if?”*—what if some existing application state failed post-deployment and we didn’t catch it?

The build went live, and for about a week, I stayed tense, waiting for something to go wrong.

Nothing did.

No blocker issues were reported from existing applications. That’s when I realized I had spent a lot of mental energy worrying about a failure that never happened.

The real outcome of that experience wasn’t the absence of a bug—it was the learning. After that incident, I created a clear SOP for pre-deployment checks that must be followed before setting up backward compatibility cases. I also shared it with my teammates so the same miss wouldn’t happen again.

Sometimes the *“what did I miss?”* feeling doesn’t end with a production bug, but it still leaves us with a better process than we had before.

---


