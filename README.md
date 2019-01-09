# Tech Hive Onboarding
New developer onboarding


## Table of contents
* [Git](#git)
  * [Commit Messages](#commit-messages)
    * [Background](#background)
    * [Guidelines](#guidelines)

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
