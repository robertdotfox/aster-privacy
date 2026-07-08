# Aster — Privacy Policy

**Effective date: July 8, 2026**

> Live page: **https://robertdotfox.github.io/aster-privacy/**

Aster is a contemplative AI companion app for iOS, macOS, and Android. This policy explains what Aster does, and does not do, with your information.

**The short version:** Aster has **no account**, **no ads**, and **no third-party analytics or cross-app tracking**. Your conversations and memories stay **encrypted on your device**. To generate each reply, your message is sent to **Anthropic's Claude** — on phones, by way of **Aster's own relay service**, which forwards it and does not store it; on macOS, through your own Claude subscription. On phones, Aster also sends one **anonymous quality report** per conversation — numbers only, never your words, and nothing that can identify you. Nothing else leaves your device.

## Who this covers
This policy applies to the Aster mobile and desktop apps ("Aster", "the app", "we"), developed and operated by an independent developer (contact below).

## What information Aster handles

### Information you provide
- **Your messages** — what you type to Aster.
- **Authentication to Claude** — On iPhone and Android you don't provide any key or account: Aster's relay service holds the connection to Anthropic on your behalf. On macOS, Aster uses your existing Claude subscription through Anthropic's official command-line client, and never sees your password or token.

### Information Aster creates on your device
- **Memories** — when you share something durable, Aster may save a short memory to keep context across conversations. Memories live **only on your device**, encrypted with AES-GCM under a key held in the device's secure keystore. The text of your memories is never uploaded to be indexed; the similarity embeddings used to retrieve them are computed locally on the device.
- **Conversation history and state** — stored encrypted on the device so your conversations persist between sessions.

You can view, edit, delete, or erase all of this at any time inside the app (the Memory tab, and Settings → "Erase all local data").

## What is sent over the network, and to whom
To generate each reply, Aster transmits the prompt assembled for that turn: your message, any memories matched to the conversation, the current conversation state, and Aster's built-in governance instructions. Apart from that — and the anonymous quality reports described below — **nothing else is transmitted**: no advertising, no cross-app tracking, no third-party analytics.

**On iPhone and Android,** that prompt is sent to **Aster's relay service** — a small server operated by Aster's developer and hosted on **Cloudflare** — which forwards it to **Anthropic, PBC** to produce the reply and streams the reply back to your device. The relay exists so you don't need your own Anthropic account or key; it passes your prompt straight through and **does not store the content of your messages or replies**. To prevent abuse and gauge load it keeps only minimal, non-content first-party counters — aggregate request volume, plus a **per-install identifier** (on iOS via Apple's App Attest; on Android a random, resettable install ID) used to monitor and limit per-device usage. These hold no message content and are never sold or shared. Cloudflare transports this traffic as the hosting provider.

**On macOS,** Aster talks to Anthropic through your own Claude subscription via Anthropic's command-line client; there is no Aster relay in that path.

### Anonymous quality reports (phones only)
When a conversation ends, the iPhone and Android apps send **one small anonymous
quality report** to Aster's relay: numeric quality scores (statistically noised
on the device before sending), category counts (such as how many turns were
flagged as misread), a bucketed conversation length, the app version, and the
governance-build hash. **It never contains a word of what you or Aster said,
and no user, device, or session identifier of any kind** — the relay folds each
report into daily fleet-wide totals and discards the individual report. These
reports exist so Aster's built-in quality standards can be tuned for everyone
without anyone's conversations leaving their device. The macOS app sends no
quality reports at all.

In every case the prompt is processed by **Anthropic, PBC** under its own terms — please review their policies:

- [Anthropic Privacy Policy](https://www.anthropic.com/legal/privacy)
- [Anthropic Usage Policies](https://www.anthropic.com/legal/aup)

Aster runs no third-party analytics SDKs, advertising networks, or crash-reporting services, and does not sell or share your data. Apart from the relay — which only forwards your prompt to Anthropic, retains no message content, and keeps quality reports only as anonymous aggregates — Aster sends your data to no other third party.

## What Aster does NOT do
- No advertising and no advertising identifiers.
- No sale or sharing of your personal data.
- No third-party analytics SDKs, no advertising or cross-app tracking identifiers, no behavioral profiling, no crash reporting. The only first-party measurements are the abuse-prevention counters and the anonymous quality reports described above — numbers only, never your words, never linkable to you.
- No accounts, no email collection, no access to your contacts.
- No notifications designed to pull you back.

## Data retention and deletion
- Memories, conversation history, and your API key remain on your device until you remove them. Uninstalling the app, or using Settings → "Erase all local data," removes Aster's on-device data. (Erasing local data leaves your Anthropic API key in the Keychain/Keystore unless you choose to clear it.)
- Data submitted to Anthropic is retained according to Anthropic's policies, not ours — we keep no copy.

## Children's privacy
Aster is not directed to children under 13 (or the minimum age of digital consent in your jurisdiction) and does not knowingly collect personal information from them.

## Security
On-device data is encrypted (AES-GCM) with keys held in the platform secure keystore (iOS Keychain / Android Keystore). Requests to Anthropic use HTTPS. No safeguard is perfect, but Aster minimizes risk by keeping your data on your device and collecting nothing centrally.

## Your choices and rights
Because Aster stores your data on your device and we hold none of it, you control it directly — read, edit, and delete it within the app at any time. For data you have sent to Anthropic, exercise your rights through Anthropic per their privacy policy.

## Changes to this policy
We may update this policy as the app evolves. Material changes will be reflected here with a new effective date.

## Contact
Questions, requests, or concerns: **robertdotfox@gmail.com**
