
[← back to README/table of contents](README.md)


# myappmaker goals


## What are myappmaker goals?

It is important to keep in mind the goals of the project, so it can be properly developed towards them. Knowing the goals of a project not only provides more context into what it is meant to become in the future, but also more information about how its design must be adhered to ensuring the software stays healthy and maintainable and its development is also healthy and sustainable.

myappmaker goals are:

- remain as simple and lightweight as possible, running smoothly in low-spec hardware
- be able to take advantage of high-spec hardware when available
- validate changes made by having the target userbase test it often
- promote healthy moderately-paced development focused in simplicity and cleanliness of design

In the following subsections we'll discuss each of such goals in detail as well as the intrinsic relationship between them. We'll also present some of the measures taken and decisions made to help achieve such goals.



### Remain as simple and lightweight as possible, running smoothly in low-spec hardware

To be inclusive, a tool must be usable in a wide range of hardware, including low-spec hardware. As such, the app must be kept reasonably small, simple, and use computer resources sparingly and reasonably. This also contributes for a better user experience and to decrease/eliminate loading times.

Software which require large amounts of RAM memory and disk space must justify their need for such resources, rather than impose such requirements on users.

There are even more important reasons for this goal, though:

- education and innovation can sprout from any environment
- environments with many limitations are very prone to innovation and development as well

We never know from which direction innovation and new developments/contributions will come, so it is vital that we do not exclude this kind of environment as well.

Projects from the Indie Python project themselves are the result of many hardware limitations faced by me (Kennedy). Were not for such limitations, those project would likely have been built on top of more complex and resource-demanding libs/frameworks and be subject to many overengineered design decisions that would exclude a lot of people reliant on low-spec hardware.

Further note that the Raspberry Pi is a potential development system, and even more likely deployment platform.



### Be able to take advantage of high-spec hardware when available

Although the first goal regards the app's suitability for low-spec hardware, people using high-spec hardware should not be left out.

It is probably something that can be explored via many different measures that should be taken as the app evolves and opportunities are perceived, like new widgets or other features that can take advantage of hardware acceleration.


### Validate changes made by having the target userbase test it often

As discussed in the section about the challenges to its development, myappmaker is threading a difficult path of trying to find an intuitive representation of what low-code/no-code app making should be.

As such, accepting changes just cause they work or even cause they are based on the design is still no guarantee of the success of the app. Only by having people from the target userbase test and approved the changes we can ensure the app is effective in its purpose of making it really easier for people to create apps. Such target userbase would mostly be comprised of people with little to no programming experience, but might as well be comprised of people who despite the experience in programming are looking for quicker and easier ways to develop apps. A truly formidable challenge.



### Promote healthy moderately-paced development focused in simplicity and cleanliness of design

Software development nowadays is plagued by freneticism. Deadlines are not guidelines to assess our performance and motivate us anymore. Instead they are shackles that menace the quality of our code. We rush our development tasks for no apparent purpose other than to pretend we are in control. And what is the reward? What do we gain by rushing our work? Just another task, just more work.

Naturally, in a commercial setting we invariably have to honor deadlines. After all, others depend on our work as well. But if the rush harms the quality of our work or leaves no room for rethinking our practices and updating our mindsets regarding problems and design, than the speed is a disservice.

In an open-source project like this one, devoid of the urgency of commercial projects, plans and deadlines are means to an end. They act as a compass to help us reach our goals. We still strive to reach our deadlines, but also have no problems postponing them, or the plans/goals themselves when needed. There are 02 reasons for this.

First, we prioritize the quality, simplicity and cleanliness of our design, the maintainability of our code. Although commercial projects have good reasons to be dead set on meeting deadlines, there's no denying that the final quality of the deliveries may suffer greatly. An open-source project, on the other hand, does not need to worry about that. Of course, an open-source proejct still has patrons who donate to the project and a userbase that follows its development and requests new features and fixes, but, as long as we are transparent in our process, communicate often and use our flexibility in a reasonable way rather than abusing the patience of patrons/community/userbase, we can focus on the quality of the development process and adjustment our deadlines as required.

The second reason is that, as a relatively new and still small open-source project, we are still underfunded and understaffed. The work done on the Indie Python project and its child projects is mostly underpaid volunteer work, mostly from me but also from other volunteer that contribute code and ideas from time to time. This lack of structure and budget makes it harder to keep planning and development up to speed in comparison to commercial projects that has paid workforce and budgets at their disposal.

As I always emphasize when speaking about this underfunded and understaffed state of the project, this is not a complaint. Working in open-source is an infinite source of fun and learning. However, to prevent issues like overburdening and burnout, we need to realize our limitations and plan accordingly. By doing that, we ensure a sustainable development process, providing a continuous stream of features and fixes.

That's why it is so important that we seek the goal of promoting a healthy moderately-paced development that focuses in the quality of our software's design, that is, its simplicity and cleanliness. Ultimately, this also contributes to its maintainability and indefinite long-term usage.

These are several concrete measures that can be taken to put all of this into practice, although we didn't decide on any of them yet:

- development in short finite periods (a couple months)
- development focus in a small set of features each time
- use a devlog for picking changes in advance and document progress over the time:
  - work to be done is submitted in advance for approval by the community as a post in the discussions tab of the repo
  - in the same post, updates are posted as the work progresses and/or adjustments are made to the work or deadlines

In conclusion, despite acknowledging our limitations, we don't use them as an excuse to be sloppy in our work. Instead, we use simple but effective measures to structure and plan our work accordingly, communicating with the community and keeping changes and improvements to our project constant. All of this in order to pursue our goal of promoting a healthy and moderately-paced development focused in simplicity and cleanliness of design.


