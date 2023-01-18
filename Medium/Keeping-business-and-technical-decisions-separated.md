# Why Bürokratt keeps its business goals and technical developments separated

> _This is an article of a series covering the business decisions of Bürokratt's not-so-common development practices_

## Background

Until the summer of 2022, technical developments of Bürokratt took place hand-in-hand with the business and technical teams on a daily basis. It's the usual way of doing things - groom 1, maximum 2 sprints ahead depending on the business requirements set or changed by that time.

It's perfectly fine if you have a small number of partners and your business requirements change a lot or are not otherwise clear by the time of publishing your procurement.

But with having 25 outsourced partners and the number growing, **paying by the hour, including for onboarding, re-onboarding** when the team members change, etc, this really **isn't an option.**

## Problem to solve - fix the scope

So we had to find a way to pay a fixed sum for the agreed outcome. This means that **the scope has to be fixed,** there's no way around it. And let's face it - the scope rarely changes for any other reasons than the business ones.

In the summer of 2022, we made an agreement within our team to **not pass any of the work to the technical team** (including the architect) **to review until the business scope had been fixed.** You might think that the logic behind it is to reduce the workload of the architect, but no. The value comes from business teams focusing on what really matters - how the product should look and feel, not how and what it's running on.

Up to that point, we didn't even have correct user stories and acceptance criteria because there was simply no need for it - all parties were involved during the 1-2 week sprint and the tasks were then forgotten.

Now, product owners, etc worked on business-level user stories and AC from weeks to months **without anyone telling them that "it would be easier to develop if we skipped this one and trimmed these 5 ones".** No more kind-of user stories stating the business need to fetch data from a Postgres database or use React instead of Angular. Only actual user stories and AC stating what the end result must look and act like.

## Lessons learned

For about 2+ months now, we have been actively developing again, resolving, and/or grooming ca couple of hundred issues. Technical grooming, as always, is a place for discussions and agile thinking. But I don't recall changing user stories other than typo fixes or making just some minor changes to business-level AC.

This means that we can and have been able to **keep our promise to our partners to not widen the scope.**

On the other hand, it also means that the business side has to put a lot more effort into the initial planning and validating results against their own AC. But really, what's the alternative?

## Next steps

We have set ourselves a goal of **an architect** pretty much completely **stepping out the development process after the whole board has been groomed** with the technical team. We are not there yet and it can probably never be fully achieved, but we are getting close to it.

## Call for action

If any of this makes you curious, be it on a business or technical level, contact us via buerokratt@ria.ee or any of the team members directly and let's have a chat.

## Next - reasons behind our technical choices

In our next article, we cover the logic of how we choose our technical stack and which criteria have to be met to take new components into use or replace/duplicate the existing ones.

> Rainer Türner<br>
> Bürokratt architect<br>
> Information System Authority of Estonia
