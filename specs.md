# Fedi Mod Specifications

This document outlines what is involved in the development of a Fedi Mod including specifications and integration points that will evolve as the ecosystem of Fedimints matures.

For now there will be three phases for the development of this spec:

![Screenshot 2023-07-17 at 7 34 10 PM](https://github.com/setlife-network/fedi-mods/assets/4914611/a08515a3-0172-46dc-afb8-c68c4f662839)

# Phase 1

Fedi Mods (FMs) are [WebLN](https://www.webln.dev/)-compatible apps that can run in Fedi's mobile web browser.

They are served like any normal web app from within the Fedi native app which uses [react-native-webview](https://github.com/react-native-webview/react-native-webview) as its web browser.

[react-native-webln](https://github.com/fedibtc/react-native-webln) is used to inject the `webln` object into the loaded web app's `window` object, serving as a WebLN provider to request and pay Lightning invoices via the user's Fedi wallet.

To access or test a Fedi Mod, download the latest version of Fedi Alpha from [here](https://www.fedi.xyz/builders).

After joining the Signet federation, go to the Settings screen and locate the bottom section labeled "General".

Tap the word "General" 10 times to access the **Developer Settings**.

From here you can add your own custom Fedi Mods for testing within the Fedi web browser and they will immediately appear on the Home screen.

## Fedi Mod Interface

The Fedi Mod browser provides function handlers for each of the following WebLN messages.

```typescript
enable(): Promise<void>
getInfo(): Promise<GetInfoResponse>
makeInvoice(data: string | number | RequestInvoiceArgs): Promise<RequestInvoiceResponse>
sendPayment(data: string): Promise<SendPaymentResponse>
```

Check the [webln interface](https://github.com/joule-labs/webln/blob/master/src/provider.ts) for more detailed type definitions.

There is also (non-WebLN) LNURL-Auth functionality that [scans the page](https://github.com/fedibtc/react-native-webln/blob/master/lib/inject-txt.ts#L75) for a-tags containing a `lightning:` uri and immediately attempts to authenticate the user according to the [LUD-04 auth base spec](https://github.com/lnurl/luds/blob/luds/04.md)

These WebLN functions are not yet supported:

```typescript
signMessage(data: string): Promise<SignMessageResponse>
verifyMessage(signature: string, message: string): Promise<void>
```

# Phase 2

...

# Phase 3

...
