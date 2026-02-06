# Day 6 – #28DaysOfTesting

Yesterday was about curiosity saving releases.  
The extra test.  
The gut check.  
Trusting your instincts.

Today is about what happens after there are no more tests to run.

The release is out.  
The pipeline is green.  
Your test cases have passed.

And yet you still cannot close your laptop.

You are scanning logs.  
Refreshing dashboards.  
Maybe even checking production in your pyjamas before breakfast  
(thanks Sara Åkerlindh for sharing that feeling).

That post release anxiety never fully goes away.  
Not after two years.  
Not after eighteen.

---

## Day 6 Challenge

Describe a time when you shipped something and had that feeling of missing something.

What happened next  
A bug in production  
Or worry for nothing

---

## My Story

In one of my earlier projects, we used to create backward compatibility cases for every release. Some cases were generic, while others were specific to the sprint features. The idea was to leave the application in different states before deployment and after deployment take those states to a terminal state to ensure everything worked as expected.

During one particular release, I missed a basic step. I did not verify the build number before setting up the backward compatibility scenarios. Later, when I asked the DevOps team to deploy the latest build, they informed me that the latest build had already been deployed at someone else request. Rolling back to the previous build was not simple. It required taking a snapshot from the production build and deploying again, which was time consuming.

Given the situation, we decided to skip the backward compatibility cases and proceed with sanity testing. Sanity testing passed, but the anxiety remained. For several days, there was a constant feeling of doubt about whether any existing application state could fail after deployment and remain unnoticed.

The build went live, and for about a week, I stayed tense while waiting for something to go wrong.

Nothing happened.

No blocker issues were reported from existing applications. That is when I realized I had spent a lot of mental energy worrying about something that never failed.

The real outcome of this experience was not the absence of a bug but the learning. After this incident, I created a clear standard operating procedure for pre deployment checks that must be completed before setting up backward compatibility cases. I also shared this process with my teammates so the same mistake would not happen again.

Sometimes the feeling of missing something does not end with a production issue, but it still results in a stronger process than before.

---


