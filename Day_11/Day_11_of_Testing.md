# Day 11 of #28DaysOfTesting

Quick question: do you know how much of your codebase was written by AI?

Not a trick question. Most teams do not know yet. Developers use tools like Copilot or Claude Code, whatever feels fastest. Sometimes they mention it. Often they do not. The merge process can easily hide it.

Here is why that matters for testing.

GitGuardian analyzed around 20,000 repositories where Copilot was active and found a 40 percent higher rate of secret leaks compared to average repositories. Hardcoded credentials. API keys in plain text.

Another study found that roughly one in three AI generated code snippets on GitHub contained security weaknesses. Not style issues. Security weaknesses.

So here is my blind spot. I have been testing code the same way for years, regardless of who or what wrote it. Maybe that was fine earlier. But I do not think it is enough anymore.

With millions of lines of code changing and self healing tests becoming common, we need to actively verify that user flows still work, buttons are not hidden behind overlays, and languages or behaviors have not silently changed.

What about you?

What are you doing differently to test AI generated code?

Or honestly, are you doing nothing different yet?



# What I Do Differently

As AI is being used more in development, I feel regression strategy cannot remain exactly the same. It is not about testing more, but about being more careful about what we test.

Earlier I was mostly focused on feature validation. Now the focus has shifted more toward analyzing the risk associated with that feature. Especially in critical areas like authentication or payments, even a small AI generated change can have a bigger impact than large changes in low risk areas.

AI does not understand the complete business context. Sometimes the code looks correct and works at first, but when we go deeper or test connected modules, we realize how much can actually be broken. The issue is not only defects, but incorrect assumptions.

Even if thirty to forty percent of the code is written by AI, the testing scope does not just increase in size, it increases in uncertainty. Because of that, I would strengthen integration testing, negative scenarios, and boundary checks instead of simply increasing coverage.

So overall, the shift for me is from testing features to consciously testing risks and assumptions.
