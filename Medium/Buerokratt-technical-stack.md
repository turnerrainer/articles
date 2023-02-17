# Business decisions behind Bürokratt's technical stack

> Bürokratt is an initiative to, in the end, provide all of the Estonian government e-services (about 3,000 of them), plus potentially any of the private sector ones, via both text-based and voice input.

To achieve this, we have made some (technical) decisions, which don’t always follow the expected path of conventional public sector procurements and technical developments. This is the fourth article of the series to cover the business values behind such decisions.

## Scope of this article

This article is not about listing all the technical tools we are using - this is subject to change and is best tracked by https://github.com/buerokratt/Buerokratt-onboarding.

Also, reading a previously published article ["Reasons behind Bürokratt giving less freedom to developers"](https://medium.com/digiriik/reasons-behind-b%C3%BCrokratt-giving-less-freedom-to-developers-fc04b0751) helps a lot to get the context.

The scope of this article is to give a higher, business level overview mostly for anyone interested in using their own stack instead of Bürokratt's default one.

## Specification-driven development

This is the key. In short, technically, you can replace every single component we have with anything you like as long as you follow the protocol. If you want to adopt new components using different protocols, you can use [DataMapper](https://github.com/buerokratt/DataMapper) (based on [Handlebars](https://handlebarsjs.com)) as an intermediate layer to switch protocols.

This means that if you have your own chatbot, you can make it communicate with Bürokratt without doing any developments other than on DSLs (text-based configuration files). At least from Bürokratt's perspective.

_When it comes to endpoints being described in the format of [OpenAPI](https://www.openapis.org), we started running before we learned to walk. As all of our services (including every single database query) are described as DSLs (text files), we can automate creating OpenAPI specs for everything we have now and all the to-be services created as mocks in the future. We are yet to have these developments and don't plan to do it manually in the meanwhile._




.................

## GitHub

Bürokratt is public as much as possible. We use [public GitHub](https://github.com/buerokratt) for plannings, developments, etc.

We are also adopting GitHub [Actions](https://docs.github.com/en/actions), [Packages](https://github.com/features/packages), etc step-by-step.

So, GitHub is our preferred tool for developments, be it planning or actual development.




## Warrany period

## Bürokratt's technical stack

The logic behind choosing Bürokratt's technical stack is previously largely covered by [Reasons behind Bürokratt giving less freedom to developers](https://medium.com/digiriik/reasons-behind-b%C3%BCrokratt-giving-less-freedom-to-developers-fc04b0751).

This article is to cover some of the mis- and lack of understandings of choosing and using Bürokratt's technical stack.

## Keeping things simple

The main goal of keeping our technical stack as minimal as possible is to keep things simple. And by "things" I mean development

## Maintenance is the key

## You can replace everything with your own

## Pentesting

## Core functionality
