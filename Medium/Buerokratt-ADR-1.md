# Reasons behind Bürokratt giving less freedom to developers

_Bürokratt is an initiative to, in the end, provide all of the Estonian government e-services (about 3,000 of them), plus potentially any of the private sector ones, via both text-based and voice input._

_To achieve this, we have made some (technical) decisions, which don't always follow the expected path of conventional public sector procurements and technical developments. This is the first article of the series to cover the business values behind such decisions._



## Problems to solve

When it comes to any software development, the most often fails are running out of money and taking way too much time  before getting an impactful result. Because, you know, computers, complexity, etc.


We at Bürokratt have no idea if we'll have 100 or 10,000 clients a year from today, but we do know that we have to provide them both a smooth on- and offboarding whenever they feel like it, also allowing every single one of them to hand-pick just the right services for them. All of our clients have to be able to join the network to provide each other's services, take part of swarm learning, update their technical stack on a daily basis, etc. And not to mention natural language processing! All this in a highly hostile environment security-wise as Bürokratt is an ML-based automated gateway to (at least) government databases and e-services.

Taking all this into account, Bürokratt, by its nature, must be an R&D project.

## Less freedom to developers

To actually be able to focus on R&D, we have taken a very strict approach on not spending our resources on repetitive, numb developments. For instance, you can't really revolutionise simple database queries but you can definitely turn them into a long-term maintenance nightmare on so many levels.

To avoid such traps, we have decided to focus on a set of generic components taking care of the most common functionalities you might expect during software development. We call such components part of Bükstack.


### Boring text files instead of actual programming

In most cases, our developers never get their hands on actual source code in its traditional meaning. Instead, creating services for Bürokratt is just a boring text files manipulation. In general, such approach is called using DSL ([Domain-specific language](https://en.wikipedia.org/wiki/Domain-specific_language)).

For us, this results in having a total control and visibility over what and how is done. For instance, every single database query we have, sits in its own separate text file. Open this text file-related URL in your browser and you see the actual result. Use this same URL in your other, even hidden services - works exactly the same way. Simple as that. And what's most important - costs just pennies compared to the traditional way of getting the same result.


### Developers still want to write code

But they can't. Usually.

When onboarding new partners, we often hear that such approach is highly uncommon and would take too much time for developers to adopt instead of just writing a new solution. The latter is exactly what we are fighting against.

After getting pass that, developers say that it's just too boring to work on text files instead of actually writing new code. We see this one as a happy problem.


### DSLs significantly lower the costs

It goes both for creating new services and keeping them up-to-date, not to mention much faster [time to market](https://en.wikipedia.org/wiki/Time_to_market).

We foresee at least tens of procurements for the next year alone. By using DSL-based developments, at least our own core team is always fully aware of what kind of components should be used, why they should be used and how much resources would it make sense to take. It means that planning and tracking technical developments can be done by the whole team, not just the architect.

Second, we can easily and very fast replace the core source code of all of our DSL-based components while not changing the DSLs themselves. This means that there's no need to re-create e-services existed so far even if the whole source code has been fully replaced.

Feel like replacing Java with Go in 2 weeks without telling anyone? Technically - no problem. Sounds like a far-fetched hypothetical situation? Not really if thousands of our clients could spend less on cloud fees just because of us deciding to switch to some other programming language.

Also, by having every single service described as a DSL, (automated) testing of new, alternative solutions becomes super easy and cheap. You can't miss it if something stopped working or produces different kind of output compared to the previous solution.

Not to mention security - DSLs are very strict, which make it possible to use fully allow-list-based security and threat hunting rules. You can not do it by adding new custom code on a daily basis.


## Call for action

If any of this makes you curious, be it on a business or technical level, contact us via buerokratt@ria.ee or any of the team members directly and let's have a chat.


## Next - open development

In our next article, we cover the concept of open development that we have already fully adopted. As a sneak peek - everything we do can be seen at https://github.com/buerokratt - no private repos, hidden task management, etc.
