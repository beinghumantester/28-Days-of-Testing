
# Day 13 of #28DaysOfTesting

"I thought YOU tested that."

Five words that can sink a release.

We have all been in that meeting. Something breaks in production. Everyone looks around the table. Nobody owns it because nobody clearly agreed who would.

The handoff problem is not really about blame. It is about assumptions. Somewhere between "dev complete" and "ready for release," testing quietly becomes everyone’s job and no one’s responsibility at the same time.

Today’s challenge: share your worst "I thought YOU tested that" moment. What broke? Who got blamed? And more importantly, what changed after?

The painful stories often teach us the most.




# What Devlopers thought I had tested but I didn't

In one of my projects, a new feature was introduced that impacted multiple existing features and all those existing features were using radio buttons. The developers shared a list of features that were expected to be affected, and based on that, I focused my testing on the new feature and the mentioned impacted areas. One feature was not included in that list. Since there were already several test cases covering the impact, I skipped testing that particular configuration.

After deployment, the client reported a critical issue. No matter whether the feature was turned on or off, there was no change in the flow. As we began debugging, we discovered the root cause. For that feature, a global configuration had been set instead of a local one. Because of that, toggling it had no effect at all.

The first reaction from the developer was, “I thought you had tested it.”

That moment was not really about blame. It was about assumptions. The developer assumed I would test every related configuration. I assumed the impact list was complete. The gap existed in what neither of us questioned.

What changed after that was simple but important. We stopped relying only on shared lists and started reviewing configuration dependencies together before calling anything ready for release. Impact analysis became a collaborative activity instead of a silent handoff.

Because testing should never become everyone’s job and nobody’s responsibility at the same time.





