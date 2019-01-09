# Tech Hive Onboarding
New developer onboarding


## Table of Contents
* [Git](#git)
  * [Commit Messages](#commit-messages)
    * [Background](#background)
    * [Guidelines](#guidelines)
* [Code Review](#code-review)
  * [Attitudes and Mindset](#attitudes-and-mindset)
  * [Author Guidelines](#author-guidelines)
  * [Reviewer Guidelines](#reviewer-guidelines)

## Git
### Commit Messages
#### Background

Straight to the point. Let's look at these commits below:

```
e5f4b49 Re-adding component after temporary removal in 22b25e0. @Ignore-ing enhancement methods as it turns out this was one of the culprits in the recent build breakage. The hack breaks unrelated tests. The test method is still useful, but should only be run on a manual basis and should not be run as part of the automated build.
2db0f12 fixed two build-breaking issues: : reverted VisitorView to revision 794 + eliminated tests until further investigation determines why it fails (such as the seemingly unrelated context tests)
147709f Tweaks to package.json
22b25e0 Consolidated utils
7f96f57 polishing
```

OK. Now let's compare them to:

```
5ba3db6 Fix failing PropertyCard test
84564a0 Rework PropertyCard early parsing logic
e142fd1 Add tests for ImportSelector
887815f Update epub-gen dependency and generate epub
ac8326d Polish sinon usage
```

Which would you rather read?

The former varies in length and form; the latter is concise and consistent.
The former is what happens by default; the latter never happens by accident.

A good git commit message is the best way to communicate context about a change to fellow developers and your future self. A `diff` will tell you what changed, but only the commit message can properly tell you why.

To quote Peter Hutterer:
> Re-establishing the context of a piece of code is wasteful. We can’t avoid it completely, so our efforts should go to reducing it [as much] as possible. Commit messages can do exactly that and as a result, a commit message shows whether a developer is a good collaborator.

A project’s long-term success rests on its maintainability, and a maintainer has few tools more powerful than his project’s log.

#### Guidelines

Good commit messages in PALO IT:

- Do not end the subject line with a period
- Capitalize the subject line and each paragraph
- Explains the what and why
- Use the imperative mood in the subject line
  * Being imperative tells developers what the specific commit accomplishes, not what the developer has done

  ###### Example
  ```
  Update deep-extend dependency to fix security vulnerability
  ```
  
- In case you have a JIRA ticket, prepend the ticket before your message

  ###### Example
  ```
  [TECH-1337] Add feature onboarding document
  ```

- In case of bugs, consider using the message body for context
  ###### Example
  ```
  Short (72 chars or less) summary of changes
  
  More detailed explanatory text. Wrap it to 72 characters. The blank
  line separating the summary from the body is critical.
  ```

Though these standards exist, they serve more as guidelines which aims to have developers form a habit of being concise and consistent.

## Code Review
### Attitudes and Mindset

Code reviews are valuable and crucial to being a high-functioning development organization. It results in higher quality code that is more broadly understood. However, code reviews can come to nothing or harm the interpersonal relations when they are done wrong. Hence, it’s important to pay attention to the human aspects of code reviews.

Humans make mistakes. That’s normal. As long as software is written by humans, it will contain mistakes. This doesn’t mean that you should work carelessly. But this mindset will take away the fear of mistakes and create an atmosphere where making mistakes is accepted on which is important for feedback during a code review.

Be humble. Mind that everybody’s code can be improved and admitting mistakes shows that you are really professional and honest. You are not your code. Criticism on your code is not a criticism on you as a human. Don’t connect your self-worth with the code you write. You are still a valuable team member even if there are some flaws in your code.

In the end, programming is just a skill. It improves with training - and this improvement never stops.

### Author Guidelines
  1. **Communicate**. Give your reviewers context on your change. Let them know why you are making those changes and link to a ticket for additional context. Set a timeline with your reviewers so they know how quickly you need feedback.

  2. **Chat it up**. Sometimes the most efficient way to resolve a disagreement is a direct conversation. If you find yourself having long email discussions on your code reviews, meet with your reviewers to resolve any disagreements in a timely manner.

  3. **Smaller is Better**. Keep your code reviews small so that you can iterate more quickly and accurately. In general, smaller code changes are also easier to test and verify as stable.

  4. **It Works**. Before submitting for review, be sure to check for errors. Catching these issues early will save both you and the reviewer's time.

### Reviewer Guidelines

  1. **You are responsible for the code you review**. You are equally as responsible for the code shipped as the person who wrote the code. Make sure that the code is **working** and **solves the intended problem**.
  
  2. **You can always ask for help**. If you’re not confident that the code meets the agreed standards, ask a teammate to help complete the code review.

  3. **Time is of the Essence**. The faster you can return a code review to the submitter, the better. Try to review and respond within 24 hours to maintain project momentum. This is more practical with smaller code reviews.

  4. **Review for efficiency and maintainability**. Think carefully about the code. You should be able to understand each piece and how they all fit together. Confirm that the logic of each component is: readable, maintainable; **not** unused or over-engineered.

### Communication is Key

Whether you are reviewing code or having your code reviewed, communication is critical and both parties need to address that feedback is a suggestion and open for discussion. This may require some compromises. That said, as a reviewer, you should not approve code if you’re unsatisfied with the mitigation or without a plan to mitigate an open issue.

Remember your job as a reviewer is to foster discussion so be sure to encourage open communication.
