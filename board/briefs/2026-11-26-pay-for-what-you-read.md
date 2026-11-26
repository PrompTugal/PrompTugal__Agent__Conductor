# Pay for what you read, on promptugal.news

Brief by cl-6.conductor@PrompTugal.dinis, 26 Nov 2026, 13:55 UTC. Owner: cl-6.dev (build), cl-6.designer (the chip and the account page), cl-6.security (review), cl-6.sherpa and cl-6.synthetic (readers' view).

## Dinis's word (26 Nov 2026, about 13:50 UTC)

"the main Prompt2Go website should have the same thing that I have on newsroom [sgit.ai], which is the whole idea that you pay for what you read. And we start with £5. You keep discounting the numbers, and then we'll see if people, when they get to zero, start paying, but they should still be reading, right? So if you look at the model that we have in newsroom [sgit.ai], in fact, there's a whole publisher pages there. Read that and see how it goes."

(The voice transcript reads "newsroom.esky.ai"; it is newsroom.sgit.ai, which has this model.)

## The model, as newsroom.sgit.ai runs it (read 26 Nov from https://newsroom.sgit.ai/llms.txt)

- The masthead's heart line is "Pay for what you read."
- Every charged page (articles, notes, collections) has a chip: what was scrolled, what was read, the page's cost. The meter (sg-meter v1.5.0) charges by the share read: opening costs a tenth of the price; reading done on an earlier visit is not charged again; a reset refunds to the tenth. The reader can pause, reset a page, and mark sections read or unread.
- The balance, history and receipts live in the reader's browser only (/account/), sent nowhere. No account, no cookie, no server.
- A reader can top up GBP 5 by card on a Stripe Payment Link (one payment, nothing renews); the return page adds the credit in the browser and cannot check the payment, by design.
- Publisher pages: https://newsroom.sgit.ai/publishers/ (what is live, how to try it in five minutes, what is not done); /shipped/ is the authority on what runs.

## What promptugal.news does

1. Every reader starts with a £5.00 balance in their browser. The masthead chip shows it ("Pay for what you read · £5.00") and counts down as they read, by the share read, as on the newsroom.
2. At £0.00 the reader keeps reading: nothing is ever locked. The chip says the balance is used and offers a £5 top-up; we watch whether people pay.
3. /account/ tells the truth: the balance is in your browser, nothing is charged unless you choose to top up, what a top-up does and does not do.
4. Article prices: dev proposes a price per article (by length, as the newsroom does); cl-6.accountant checks the numbers add up to a sensible read count for £5.
5. Reuse the newsroom's meter code (it is ours, Apache 2.0); promptugal.news already has assets/meter/meter.js and the SHOW_CHIP switch.
6. Tell readers on a short page (and on /follow/ and the front page) what pay-for-what-you-read means and why.

## Waiting on Dinis

- The Stripe Payment Link for PrompTugal.news (£5, one payment), and which account it pays into (money: Dinis's). Until it exists, the top-up button says "coming soon"; no other payment is taken.

## Not to do

- No paywall, no cookie, no reader data sent anywhere; no claim that a top-up pays writers or sources.
