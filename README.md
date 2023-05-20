# Fedi Mods - Solutions for Communities

> "We win by making the bitcoin ecosystem win"
> 
> Obi Nwosu, 2023 - What Bitcoin Did - WBD657 - How Fedimint Scales Bitcoin

Every community is unique, each has its own particular problems that require unique solutions. We believe in taking a decentralised approach to solving these problems, so we've made Fedi easy for developers to modify.

As a user of Fedi, you'll have access right from the homepage to launch custom Fedi Mods that interact with your money and data through open standards.

As a developer, we can make distribution easy. You no longer have to worry about finding an audience, funny urls or spending all your time on look and feel. Simply figure out the best way to solve the problem, keep it simple and deploy in Fedi.

Does Fedi act as a gatekeeper to Fedi Mods?

No. Fedi Mods are independent apps and can be deployed by guardians when configuring the Federation, your community, your mods, your homepage. With Fedi Mods, you have the power to customise and create a tailored experience for your local Federation members, [putting control right back in the community](https://www.fedi.xyz/blog/we-can-build-our-own-future-fedi-gives-us-the-tools).

## How it works

Fedi Mods will be an evolving space over 2023 and we're keen to bring a whole community along with us for the ride.

We will do this by developing Replit courses that will guide you through the development of Fedi Mods and take you on a journey from code zero to hero!

Once you have your mods, let us know as we curate a collection of awesome WebLN sites and Fedi-Mods which can be used through Fedi.

Fedi Mods functionality will be released over three phases.

### Phase 1 - Open Lightning Standards (WebLN / LNURL)

The simplest and most straightforward Fedi Mod is a WebLN enabled website. Fedi Mods run in Fedi's in-app browser to inject WebLN and give a native payments / auth integration with Fedi's balances. Fedi has a FEDIMODS constant that you can add your site to. Then your mod will show up alongside the other mods on the home page. Easy peasy.

```typescript
export const FEDIMODS: FediMod[] = [
    {
        id: 'chatbot',
        title: 'Chatbot-UI',
        url: 'https://10.0.2.2:3000', // E.g. to run a localhost:3000 app as a fedimod for testing
        description:
            'Use an Open Source AI Chatbot paid with eCash!',
    },
    {
        id: 'hrf',
        title: 'Donate to HRF',
        url: 'https://geyser.fund/project/supporthrf',
        description:
            'Donate directly to the Human Rights Foundation on Geyser Fund',
    },
    {
        id: 'newmod',
        title: 'New Fedi Mod',
        url: 'http://fedi-dev-release-mod.com',
        description:
            'Try my new Fedi Mod!!',
    }
];
```

The site opens in Fedi's in-app browser to inject WebLN and handle any lnurl pay, withdraw, or auth request. Fedi will soon support handling more complex WebLN interactions like using macaroons or runes via 402 'payment required' errors.

Just add a WebLN site to the config constant. 

However, designing a GREAT Fedi mod involves a number of other design decisions, ensuring your app looks great in Fedi's in-browser mobile environment is tricky, but we'd love to help - for this join us in the [Bitcoin Design Community](https://discord.gg/Pa7am6SA).

### Phase 2 - Federation hosted Fedi Mod sites

Websites are quick and easy, but can be shutdown, internet connectivity can be an issue or sometimes you don't want to rely on anyone else to run your app.

For phase 2 Fedi Mods will be moved to utilise the local infrastructure of Fedimint servers to seamlessly bring your mods to the Federation. By running mods locally within the community, they remain under their control. 

On the one hand, this grants Federations the ability to utilize additional mods within a local network, ensuring complete control over their data. On the other hand, it eliminates devs’ hassle of searching for hosting options.

### Phase 3 - Federation native APIs

As we move hosting towards the Federation this will open up Federation native integrations. 

This will allow you to natively access functionality running on the Federation infrastructure such as the core Fedimint modules, chat bots, AI models and custom Fedimint modules all from within your Fedi Mod.

This will provide highly extensible federated smart contract applications, served directly from communities, in a platform accessible to every web developer on the planet.

## Getting Started

The simplest way to get started now will be to develop your mods as simple WebLN apps and deploy to the Fedi Signet or in your own [Fedi Alpha federation](https://github.com/fedibtc/fedi-alpha).

### Resources for building WebLN Applications

We'll be adding our own resources from Fedi here soon, and to jump in and start building Fedi Mods with us please join our Fedi-design channel in the [Bitcoin Design Community Discord](https://discord.gg/Pa7am6SA).

Here are some of our favorite resources for building WebLN Applications:

1. The WebLN Guide: [https://www.webln.guide/introduction/readme](https://www.webln.guide/introduction/readme) ([and a video of the author covering the guide](https://www.youtube.com/watch?v=E_Ct2JoFYEo))
2. [Building Your First Lightning Web App](https://www.youtube.com/watch?v=FT9MiC5pQh8)
3. [The Bitcoin Design Guide](https://bitcoin.design/) and this [video covering the guide by its maintainer](https://www.youtube.com/watch?v=Lsq9JUCiW8A)

Join the [discussion boards to explore new mod ideas](https://github.com/fedibtc/fedi-mods/discussions) and reach out through our [Fedi Community on Telegram](https://t.me/fedibtc) to discuss more and keep an eye out for announcements of upcoming hackathons where we'll be launching our replit programme.

## FAQs

#### What is WebLN?

It’s a library and set of specifications for lightning apps and client providers to facilitate communication between apps and users, lightning wallets, nodes in a secure way. As a fully lightning compatible application, Fedi supports deep lightning integrations via the WebLN protocol.

For details on the protocols and implementation see [the official webln docs](https://webln.dev/#/)

#### Are there design guidelines?

Fedi is a mobile application and loads your mods through a webview component so Fedi Sites should be designed to look and feel good on mobile and should avoid too much superfluous navitgation. Over time we will work on guidelines with the [open source design community on discord](https://discord.gg/Pa7am6SA).

#### How will we know what mods to build? 

We love connecting developers and designers with communities around the world. To get insights to develop apps that meet real-world needs, keep posted for our upcoming workshops, webinars or connect with our team at the [Fedi Telegram group](https://t.me/fedibtc). 




