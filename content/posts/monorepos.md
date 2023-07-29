---
title: The curious case of monorepos vs multi-repos
date: 2023-07-29T01:41:33+02:00
draft: false
tags:
    - platform
    - devexp
    - organization
    - developer
    - monorepo
---

# The curious case of monorepos vs multi-repos

The discussion about monorepos vs multi-repos is a common one among software engineers, especially those who work in platform and developer tools. The question often comes up in the following forms: "Should we merge all our repos into one?" or "Should we split our repos into multiple repos?"

## It's not what you think.

Most of the discussions I've seen so far about monorepos focus on the following pros:

* Google uses monorepos.
* Monorepos make it easy to share code.
* You have more control over a monorepo.

Meanwhile, the pros of multirepos are often cited as:

* Multirepos are more natural.
* You don't have to create custom tools for multirepos.

However, these discussions often miss the most important point: **the problem you're trying to solve.**

## Tell me the problem, not the solution.

As software engineers, we're wired to think about solutions first, not the problem. So many people, with good intentions, end up communicating their solutions to a problem instead of the problem itself. We like to solve problems and help people, so it's hard for us to resist.

If someone in your company or organization proposes using a monorepo or a multirepo, you should always ask "why.". 
What problem are they trying to solve? What's the root problem ?

## There are no silver bullets, only costs.

When we make decisions about solutions, we often overlook the costs involved since we focus on the solution. Whatever decision you make, it will have both pros and cons. You need to carefully consider the costs before making a decision.

Here are some of the costs to consider when choosing between a monorepo and a multirepo:

* The initial cost of merging or splitting the repos or even having to support both.
* The cost of changing internal tools to follow the new structure.
* The cost of training all engineers and changing the culture to adjust to the new style.

So, considering the pros, the cons, and the cost, is it a viable decision ?

## It's an organizational change, not just a technical one.

There are two organizational considerations to keep in mind when making this decision:

1. How will this decision impact the engineers who run the internal developer tools? Any new structure will require changes to support that decision, such as merging teams, splitting teams, or creating new teams.
2. If you're moving to a multi-service world, how will the new structure reflect the business domain boundaries and accountability?

## Copy-pasting is not always good.

Don't make the decision to use a monorepo or a multirepo just because another company or open source project does. Every company has its own culture, practices, and history. If you blindly copy someone else's approach, you'll end up copying their mistakes as well.

## Change is hard, sometimes it's required, but don't make it harder.

A friend introduced me to a nice concept of "reversible" or "irreversible" decision. Simply ask yourself, can we reasonably reverse this decision later?

While sometimes the value is clear, the cost can be too great, and it might drive you to hesitate. In those cases, think about the worst case scenario: we have to reverse our decision, can it be done? If not, can we make a small experiment and measure the desired change instead of a full-blown change?

## Conclusion

The decision of whether to use a monorepo or a multirepo is a complex one. There are many factors to consider, including the problem you're trying to solve, the costs involved, and the organizational impact, decision reversibility. Don't make the decision lightly.
