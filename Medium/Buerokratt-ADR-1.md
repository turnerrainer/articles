## Business values behind Bürokratt's (technical) decisions

_Bürokratt is an initiative to, in the end, provide all of the Estonian government e-services (about 3,000 of them), plus potentially any of the private sector ones, via both text-based and voice input._

_To achieve this, we have made some (technical) decisions, which don't always follow the expected path of conventional public sector procurements and technical developments. This is the first article of the series to cover the business values behind such decisions._



## Problem to solve

When it comes to any software development, the most often fails are running out of money and taking way too much time  before getting an impactful result. Because, you know, computers, complexity, etc.


We at Bürokratt have no idea if we'll have 100 or 10,000 clients a year from today, but we do know that we have to provide them both a smooth on- and offboarding whenever they feel like it, also allowing every single one of them to hand-pick just the right services for them. All of our clients have to be able to join the network to provide each other's services, take part of swarm learning, update their technical stack on a daily basis, etc. And not to mention natural language processing! All this in a highly hostile environment security-wise as Bürokratt is an ML-based automated gateway to (at least) government databases and e-services.

All this leads to a fact that Bürokratt, by its nature, is and must be an R&D project.

## Less freedom to developers

To actually be able to focus on R&D, we have taken a very strict approach on not spending our resources on repetitive, one might even say dumb developments. For instance, you can't really revolutionise POST or GET queries but you can definitely turn them into a long-term maintanance nightmare on so many levels. The same goes for if/else statements, database queries, and so forth.

To avoid such traps, we have decided to focus on a set of generic components taking care of the most common functionalities you might expect during software development. And you must be able to use them without writing a single line of code in Java, Go or any other "actual" programming language. We call such components part of Bükstack.

### Boring text files instead of actual programming

For instance, we have 0 relational database queries written in Java or similar - every single database query of ours sits in a separate text file of its own and can be used as a standard REST call. This one is served by a Bükstack component called Resql.

We also have 0 lines of Bürokratt-specific code in our Java (or any other) applications. Every single condition(al switch), business logic, replacable endpoint, etc is defined in YAML files. We create all of our actual, natural language-based e-services, the same way a CI/CD engineer would use Docker or Kubernetes. This is provided by Ruuter, our most central Bükstack component.

We have also adopted Handlebars as a third-party component to make sure that changing data protocols - for instance, when replacing one component/endpoint with another - could be done easily on a level of, once again, text file(s). Not Java, not Go, not some other actual programming language requiring (too) specific knowledge.


Such approach has caused a lot of, let's call it attention, by a number of companies providing custom programming as a living. Even to an extent to not take part of Bürokratt's procurements for as long as using Bükstack components is a must. Which is, of course, their right.

In short, there have been 2 arguments against Bükstack. The first one is that studying Bürokratt DSL (domain-specific language to describe all of our text file-based configurations) takes too much effort. And the second one is that only creating Bürokratt DSLs is too boring for serious programmers.

For us, being based on these DSLs, is highly important. First, whenever we start with a new procurement (and we literally have tens of them every year), at least our own team already exactly knows what to use, why to use and how much resources should it take.

Second, we can easily and very fast replace the core source code of all of our Bükstack components while not changing the DSLs. Feel like replacing Java with Go in 2 weeks without telling anyone? Technically - no problem. Sounds like a far-fetched hypothetical situation? Not really if thousands of our clients could spend less on cloud fees just because of us deciding to switch to some other programming language.

Third, by having every single service described as a DSL, (automated) testing of new, alternative solutions becomes super easy and cheap. You can't miss it if something stopped working or produces different kind of output compared to the previous solution.

And these are just some of the benefits from Bürokratt's perspective. And could also be yours, if you chose to start using Bükstack as well.
