# Business decisions behind Bürokratt's technical stack

> This article is not about listing all the technical tools we are using - this is subject to change and is best tracked by https://github.com/buerokratt/Buerokratt-onboarding. Also, reading a previously published article ["Reasons behind Bürokratt giving less freedom to developers"](https://medium.com/digiriik/reasons-behind-b%C3%BCrokratt-giving-less-freedom-to-developers-fc04b0751) helps a lot to get the context.

The scope of this article is to give a higher, business level overview mostly for anyone interested in using their own stack instead of Bürokratt's default one.

## Specification-driven development

This is THE key. In short, technically, you can replace every single component we have with anything you like as long as you follow the protocol. If you want to adopt new components using different protocols, just use [DataMapper](https://github.com/buerokratt/DataMapper) as an intermediate layer.

This means that if you have your own chatbot, e-service, etc, you can make it communicate with Bürokratt without doing any developments other than on DSLs (text-based configuration files). At least from Bürokratt's perspective.

_When it comes to endpoints being described in the format of [OpenAPI](https://www.openapis.org), we started running before we learned to walk. As all of our services (including every single database query) are described as DSLs, we can automate creating [OpenAPI](https://www.openapis.org) specs for everything we have now and all the to-be services created as mocks in the future. We are yet to have these developments and don't plan to do it manually in the meanwhile._

## Warranty

### Bürokratt's core functionalities

If you are developing the core functionalities of Bürokratt, you have to use Bükstack ([read more](https://github.com/buerokratt/Buerokratt-onboarding)). That's because this is the stack we are familiar with, have continuous [pentesting](https://en.wikipedia.org/wiki/Penetration_test) on, etc. We also take the responsibilty to fix errors, add functionalities, etc within Bürokratt's services.

> PS! The latter means that Bürokratt does not take any responsibility for any projects using Bükstack components outside of Bürokratt.

### Your (custom) components replacing ours

If some of your clients are using Bürokratt and you decide to replace [Ruuter](https://github.com/buerokratt/Ruuter) with something else, there are 0 _technical_ restrictions for it. Just follow the protocol and you're good. But you have the responsibility to provide fixes, maintenance, [pentesting,](https://en.wikipedia.org/wiki/Penetration_test) deployment, etc, Bürokratt's core team will have nothing to do with it.

Also, your clients might not be eligible to be part of Bürokratt's Network if your stack fails to provide credible affirmation about being resilient to attacks, cover all the functionality, and so forth.

## Bükstack being a blocker

We develop nothing just in case. If we don't have a use case for a functionality, we don't have it. This means that over time, our partners encounter situations where Bükstack is missing some crucial functionality.

Let's say it happens with [Ruuter](https://github.com/buerokratt/Ruuter). In such cases, our partner creating a planned service creates [Ruuter DSL](https://github.com/buerokratt/Ruuter/tree/main/samples) but replaces blocking functionality with [mock endpoints](https://github.com/buerokratt/Ruuter/blob/main/samples/steps/mock.md), mimicking the to-be response.

The development of necessary [Ruuter's](https://github.com/buerokratt/Ruuter) core functionality is out of scope for this partner and is done separately. So, in such cases, there are no Bükstack-related blockers for our partners - they get their money even if the full functionality is not really there yet. And if you are creating services on a Java-based [Ruuter](https://github.com/buerokratt/Ruuter), you don't actually need to know anything about Java.

## Security

We have just recently started with continuous [pentesting](https://en.wikipedia.org/wiki/Penetration_test) of Bükstack and are working on having public bug bounties to break our code. And as all of our services are (by default) based on Bükstack, the responsibility for security lies greatly on our, not developer's side. It's different only in case of developing the core components of Bükstack themselves but these are rare occasions.
