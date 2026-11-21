# $OSTRA — Stoa Buy Card Demo

A demo page showing Stoa's official **buy card** embedded on a token page, preset to **$OSTRA** (Ostra Agent token) on Robinhood Chain.

**Live demo:** https://ranggamurphy.github.io/ostra-buycard-demo/

## What this is

- An integration example prepared for the [Stoa build bounty](https://stoadex.com/build#bounties) (bounty #2: swap widget / buy card on a token's site).
- It uses Stoa's official embed, exactly as documented at https://stoadex.com/docs/embed — no custom swap code:

```html
<iframe src="https://stoadex.com/embed/robinhood/0x68Ff81dFFF6eccefb74706fE1e0a86320CB2Eb96?ref=0x4D9F4C51935540a1efDc9Db3dbb67fBf44359775"
  width="100%" height="230" style="max-width:420px;border:0;border-radius:16px"
  title="Buy on Stoa" loading="lazy"></iframe>
```

- Token: $OSTRA, contract `0x68Ff81dFFF6eccefb74706fE1e0a86320CB2Eb96` (Robinhood Chain, chain ID 4663).
- Referrer: the `ref` parameter is the integrator wallet `0x4D9F4C51935540a1efDc9Db3dbb67fBf44359775`. Swaps started from the card carry this referrer, so the referral share (10% of Stoa's 2 bps protocol fee) is booked to that address in Stoa's FeeDistributor.
- The card shows the live price and a live route read from Stoa's router; the Buy button opens stoadex.com with the token selected and the referrer attached. No wallet connects inside the card.

## Not affiliated

This is a standalone demo on the integrator's own page. It is **not affiliated with, endorsed by, or published by the OSTRA project**, and it is not the OSTRA project's website. It exists so the integration can be previewed before anything goes live on the project's real site, subject to the project's agreement.
