# Fedi-Mods: WebLN Sites for Communities

> "We win by making the bitcoin ecosystem win"
> 
> Obi Nwosu, 2023 - What Bitcoin Did - WBD657 - How Fedimint Scales Bitcoin

Every community is unique, each has it's own particular problems and that require unique solutions. We believe in taking a decentralised approach to this, so we've made Fedi easy for develpers to modify.

As a user of Fedi, you'll have acess right from the homepage to launch custom "Fedi-Mods" to interact with your money and data through open standards like WebLN and Fedimint's module system.

For developers, Fedi-Mods are a distribution channel and design space to deploy your webln site with native payments, auth, and L402 management within Fedi's in-app browser.

Solve a problem, keep it simple, & deploy in Fedi.

- **Q:** Does Fedi act as a gatekeeper to Fedi-mods?
- **A:** How little you know us! Fedi-mods are selected by federation guardians at configuration time. Just as guardians choose which fedimint modules to run in consensus, they can select which fedi-mod sites to feature to users of their federation.

Your community, your mods, your homepage.

Fedi mods provide a simple way to provide a unique experience for your local federation members, [all under your control](https://www.fedi.xyz/blog/we-can-build-our-own-future-fedi-gives-us-the-tools). 

## How it works

Fedi mods will be an evolving space over 2023 and we're keen to bring a whole communty along with us for the ride.

We will be publishing replit courses that will guide you through the development of fedi mods and take you on journey from code zero to hero!

Once you have your mods, let us know as we curate a collection of awesome webln sites and fedi-mods which can be used through the Fedi App and to be featured as we scale bitcoin adoption to communities around the world.

Fedi-mods are fundamentally Lightning enabled websites, but can be tailored and designed to leverage fedimint modules and community scaling opportunities unavailable to standard web applications.

### Phase 1 - Open Lightning Standards (WebLN / LNURL)

The simplest and most straightforward Fedi-mod is a WebLN enabled website. Fedi-mods run in Fedi's in-app browser to inject WebLN and give a native payments / auth integration with Fedi's balances. Fedi has a FEDIMODS constant that you can add your site to. Then your mod will show up alongside the other mods on the home page. Easy peasy.

```typescript
export const FEDIMODS: FediMod[] = [
    {
        id: 'chatbot',
        title: 'Chatbot-UI',
        url: 'https://10.0.2.2:3000', // E.g. to run a localhost:3000 app as a fedimod for testing
        description:
            'Use an Open Source AI Chatbot!',
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
        title: 'New Fedi-Mod',
        url: 'http://fedi-dev-release-mod.com',
        description:
            'Try my new Fedi mod!!',
    }
];
```

The site opens in Fedi's in-app browser to inject webln and handle any lnurl pay, withdraw, or auth request. Fedi will soon support handling more complex webln interactions like using macaroons or runes via 402 'payment required' errors.

So that's the easiest way, just add a webLN site to that config constant. However, designing a GREAT fedi mod involves a number of other design decisions. Ensuring your app looks great in fedi's in-browser mobile environment is tricky, but we'd love to help! Join us in our Bitcoin Design Community channel: 

### Phase 2 - Federation hosted fedi-mod sites

Websites are quick and easy, but not for every environemnt. Sometimes you don't want to rely on anyone else to run your app or the network conectivity just doesn't work out. 

Fedi-mods can uniquely take advantage of the local infrastructure running the fedimint nodes to bring your mods to the Federation, running them locally in your community and under your control.

This allows you to operate a Federation with additional mods on a local only network or simply ensure that your data never leaves your control. In the coming months, fedimint modules allowing hosting and digital infrastructure access by federations themselves will let you design for the users of your fedi-mods to locally run and maintain the mods themselves.

### Phase 3 - Federation native APIs

As we move hosting towards the Federation we explore Federation native integration. This will allow you to natively access module functionality running on the fedimint's federation infrastructure such as core fedimint, chat bots, AI models and custom fedimint modules all from within your Fedi mod. 

Highly extensible federated applications served directly from your community, accessbile to every web developer on the planet. 

## Getting Started

The simplest way to get started now will be to develop your fedi-mods as simple webln apps and get added to federations running on the Mutiny Signet or in your own [Fedi Alpha federation](https://github.com/fedibtc/fedi-alpha). 

### Resources for buildling WebLN Applications

We'll be adding our own resources from Fedi here soon, and to jump in and start building Fedi-mods with us please join our Fedi-design channel in the Bitcoin Design Community Discord.

Here are some of our favorite resources for building WebLN Applications:

1. The WebLN Guide: [https://www.webln.guide/introduction/readme](https://www.webln.guide/introduction/readme) ([and a video of the author covering the guide](https://www.youtube.com/watch?v=E_Ct2JoFYEo))
2. [Building Your First Lightning Web App](https://www.youtube.com/watch?v=FT9MiC5pQh8)
3. [The Bitcoin Design Guide](https://bitcoin.design/) [and a video covering the guide by its maintainer](https://www.youtube.com/watch?v=Lsq9JUCiW8A)

Join the [discussion boards to explore new mod ideas](https://github.com/fedibtc/fedi-mods/discussions) and reach out through our [Fedi Community on Telegram](https://t.me/fedibtc) to discuss more and keep an eye out for announcements of upcoming hackathons where we'll be launching our replit programme.

## FAQs

#### What is webln?

It’s a library and set of specifications for lightning apps and client providers to facilitate communication between apps and users lightning wallets/nodes in a secure way. As a fully lightning compatible application, Fedi supports deep lightning integrations via the fully scope of the WebLN protocol.

For details on the protocols and implementation see [the official webLN docs](https://webln.dev/#/)

#### Are there design guidelines?

Fedi is a mobile application and loads you mods through a webview component so Fedi Sites should be designed to look and feel good on mobile and avoid to much superflous navitgation. Our advice would be to focus on a simple tightly scoped use case and avoid too much complexity - "whats the one highly valuable thign you can provide to Fedi users".

Over time we hope to develop and open source some design guidelines for the delivery of Fedi Mods and work collaboratively with these design communities and frontend developers to help adapt your webln sites to improve their UX for Fedi. 

#### How will we know what mods to build? 

We love connecting developers and designers with communities around the world to get insights to develop apps that meet real-world needs. 

We hope to build this bridge connecting developers to real-world needs and opportunities. Our Fedi Order can provide guidance on what they're hearing on the ground, what works, what doesn't, and connect you to audeinces that need your solutions.




