# EVER BLOCKCHAIN — The Abundance Blockchain

Draft 1.3 · October 31, 2026 · E-V-E-R

## Abstract

EVER BLOCKCHAIN is the abundance blockchain: a global network that gives every verified human a daily drop of tokens, starting at 240,000 a day, with no mining and no money staked. It is not built to be scarce. It is built so that every person, and the AI agents working for them, has a steady flow of tokens to coordinate with: to trade, share, and claim real resources such as energy and work through credits. The network is secured by ordinary PCs run by verified humans, picked at random each round. Every signature and proof uses math that quantum computers are not expected to break. The chain never stores a face, a name, a location, or an email; it stores only proofs. Nobody controls it after launch: four rules are fixed forever, everything else is a dial that verified humans change by vote. Version 0 runs on five computers in 2027. Version 1 adds passport-chip joining, a 15-second liveness check, and zero-knowledge proofs.

## The problem

Four things broke at once.

**Bots are now as good as people online.** AI agents pass every puzzle, write every message, and can run a thousand accounts for the price of one. Any system that hands out value per account is farmed to death within days.

**Money systems were not built for this.** Central banks, payment apps, and most cryptocurrencies all assume someone else proves you are a person: a bank, a government, a phone company. None of them can prove you are *one* person who has not signed up already.

**Money is built on scarcity.** Almost every currency, and almost every cryptocurrency, gets its value by being hard to get. That made sense when work and goods were scarce. In a world where software and agents can produce more every year, a system designed around scarcity measures the wrong thing. People need a way to coordinate what they have, not just a number that goes up because there is less of it.

**Every proof-of-personhood attempt so far has a hole.** Iris-scanning hardware needs a company to build and ship it. Social vouching lets rings of fakes vouch for each other. Timed puzzles get solved by AI. Location checks get spoofed by software and, soon, by robots. The field's own conclusion, from Ethereum's founder to the MIT and OpenAI personhood-credentials paper, is that no single method works and the only path is to stack several.

EVER BLOCKCHAIN starts from that conclusion and adds four things the others lack: a payout built for abundance instead of scarcity, a payout that makes the network pay its own guards, a design that assumes cheaters and survives them, and cryptography that will still hold in 2040.

## Joining and staying

A person joins once, then proves they are still here at a random time, at least once a year. Both take under a minute and need nothing but a modern phone.

**Join: tap your passport.** Most passports issued since 2006 carry a chip. The phone reads it over NFC, checks the issuing country's signature, and builds a zero-knowledge proof that says exactly one thing: "a real, unused ID stands behind this account." The chain stores a nullifier, a random-looking code derived from the chip, so the same passport can never open a second account. The passport data itself never leaves the phone. Countries without chip passports, and people without any ID, are a known gap addressed in the roadmap.

**Stay: Pulse.** At least once a year, at a time nobody knows in advance, the app asks the person to look at the phone for 15 seconds. The random beacon picks one unannounced day in each 12-month window, and from that day the person has 7 days to complete the check. The screen plays a color pattern; the front camera measures how real skin reflects it and picks up the pulse in the face; the depth sensor confirms a three-dimensional head. This proves a living person is still holding the phone. Nothing is recorded or uploaded; the secure chip signs a single "live human present" message.

**The certainty score.** Every account carries a score from 0 to 100. A passport join starts at 90. Passing Pulse keeps it there. Missing Pulse, odd claim patterns, or flags from the network lower it. Above 70 the daily drop flows in full. Between 40 and 69 the drop pauses. If the cause is a missed Pulse, doing Pulse fixes it; if the account was flagged, a human reviewer looks. Below 40 the account is frozen. A confirmed bot is banned and its passport nullifier is burned forever.

**What a missed Pulse costs.** Tokens already in an account are never taken by the network, under any rule.

- **Missed window:** the score drops from 90 to 60 and the daily drop pauses. The balance is untouched, and sending still works.
- **Pulse done late:** the score returns to 90 and the drop resumes the next day. Missed days are not paid back.
- **Six months of silence after a missed window:** the score falls below 40 and the account is frozen: no claiming and no sending. Passing Pulse plus a reviewer's approval unfreezes it.
- **Never returns:** the tokens sit in the account forever.

**Reviewers.** Software flags; it never bans. Verified humans who opt in make the final call and are paid from a bounty pool. A reviewer's own score depends on being right, so careless reviewers lose their standing.

Why this holds against superintelligence: an AI can imitate any behavior, but it cannot cheaply manufacture passports or living bodies. The join rule rests on the first, the stay rule on the second, and the score and reviewers catch what slips through.

## The daily drop

Every verified human can claim the daily drop once a day, at 00:00 UTC. It starts at 240,000 tokens. The rule is the same for everyone, and no person or company decides who gets paid.

- A new day opens on chain at midnight UTC.
- The phone submits a claim with a proof that the account is verified, scored above the threshold, and has not claimed today.
- The chain mints the tokens straight to the account. Unclaimed tokens are never minted; a skipped day simply does not exist. Dead accounts cannot pile up value.

**There is no total supply cap, and no halving.** Supply grows with the number of humans. Eight billion people claiming for a thousand years is about 700 quintillion tokens; any cap large enough to allow that is a number with no meaning, so the design drops it and says so plainly. This is the abundance choice: nothing in the code shrinks the flow on a timer to make early holders richer. On any given day, a person who joined that morning gets the same drop as a person who joined in 2027.

**The amount is a dial, not a law.** 240,000 is the starting point, not a promise. There is no schedule: no halving, no yearly vote, no automatic change. The community changes the amount only when it decides it needs to. Any verified human can propose a new amount at any time, and it passes under the normal voting rules in Governance. Only accounts scored 70 or above vote.

**What gives it value.** Everyone receives the same amount, so the number itself is not the point. Markets set the price, in dollars and everything else. A token is worth what people and agents will exchange for it: money, a unit of power, an hour of compute, a task done. The first use is built in: paying the people who run the network. Nodes earn 24,000 a day on top of their drop, and reviewers are paid from the bounty pool. The network pays its own guards from day one. The second use is credits, described next.

## Credits: energy and value

Tokens are the flow. Credits are what the flow can be turned into.

A **credit** is an on-chain offer, backed by someone real, to deliver something real in exchange for tokens. The chain does not produce energy or goods. It records who offers what, holds tokens in escrow, and settles when delivery is confirmed.

- **Energy credits.** A verified human or group that produces power, such as a home solar array, a battery, or a community microgrid, can post energy credits: "X kilowatt-hours, delivered here, for Y tokens." Buyers redeem tokens for those credits.
- **Value credits.** Anything else that can be delivered and confirmed: compute time, storage, bandwidth, a repair, a lesson, a translation, an agent's finished task.

**How a credit works:**

1. A provider posts an offer: what, how much, where, for how many tokens, and how delivery is confirmed.
2. A buyer, human or agent, accepts and the tokens move into escrow.
3. Delivery is confirmed: by the buyer, by a meter or device signature, or by a reviewer if disputed.
4. Escrow releases to the provider. A provider who fails delivery has the tokens returned to the buyer and their account score lowered.

**Every credit is backed by a verified human.** Providers are verified human accounts or agents owned by one. A provider's history of delivered and failed credits is public, so trust is earned in the open.

**Exchange rates are found, not set.** The protocol never fixes how many tokens a kilowatt-hour costs. Each offer sets its own price in tokens, and the market of offers finds the rate. Markets also set the token's price against dollars and other currencies, the same way they do for any other asset.

## Security without mining

Bitcoin is secured by electricity. Most newer chains are secured by money staked. EVER BLOCKCHAIN is secured by people: always-on PCs, one per verified human, chosen at random each round.

**Nodes.** A node is an ordinary computer on home internet, online at least 95% of the time. One verified human may run at most one node, tied to their account. Nodes earn a daily bonus for showing up and voting honestly. Mainnet opens with at least 1,000 nodes in 30 countries.

**How a block is made, every few seconds:**

1. The network produces a public random number for the round.
2. That number picks a committee of about 300 nodes.
3. One proposes the block; the rest check it and vote. Two-thirds must agree.
4. The block is final immediately. There are no confirmations to wait for.
5. The committee's votes are bundled into one proof that any phone can check in under a second.

**The randomness beacon.** Every committee member commits to a secret number, then reveals it, and all the numbers are mixed into one. No single node can steer the result, and a node that commits but refuses to reveal is penalized. The beacon is built from hash functions only, so it stays quantum safe. The design follows the public drand beacon; the math does not, because drand's is not quantum safe.

**Why it holds.** To forge a block an attacker needs one-third of a committee. Committees are random and drawn from verified humans, so the attacker would need one-third of all nodes, which means one-third of all verified humans with passports. The join rule is the cost of attack.

**Phones never validate.** They download one proof per block and check it. That keeps the network open to a phone on a slow connection anywhere on Earth.

## Privacy: proofs, not data

The chain never sees you. It stores receipts that something was checked, never what was checked.

- The phone does every check: the passport read, the Pulse liveness, the daily claim.
- The phone turns each result into a zero-knowledge proof, a piece of math that says "a verified human owns this account" and nothing more.
- The chain verifies the proof and keeps only a nullifier, a code that stops a double claim and cannot be reversed into a person.
- Faces, pulses, and passport data stay inside the phone's secure chip and are never uploaded.

This is the pattern World ID uses today. EVER BLOCKCHAIN keeps the pattern and changes the math: World's proofs rest on elliptic curves that quantum computers are expected to break, so this network uses STARK proofs, which are built from hash functions alone.

The few things that must be shared, such as the evidence in a review of a flagged account, are split by secret sharing across random members so that no single piece reveals anything.

## Quantum safety

No elliptic-curve cryptography appears anywhere in the network. Every signature, proof, and key exchange comes from the two families now standardized by NIST: lattices and hashes.

| Part of the chain | Scheme | Standard |
| --- | --- | --- |
| Account signatures | ML-DSA-65 | FIPS 204 |
| Governance keys | SLH-DSA | FIPS 205 |
| Committee votes | Hash-based XMSS, bundled into one STARK | Ethereum's post-quantum consensus plan |
| Zero-knowledge proofs | STARKs | Hash-based |
| Hashing | SHA-256, Poseidon2 | |
| Key exchange | ML-KEM | FIPS 203 |

The cost is size: an ML-DSA-65 signature is 3,309 bytes, roughly 50 times today's 64-byte signatures. The network pays that cost once per transaction and avoids it in consensus by bundling committee votes into a single proof.

No post-quantum scheme is proven beyond doubt, so every account is a smart account that can switch signature schemes by vote. If one scheme falls, the network moves to another without losing a single account.

The United States has set December 2031 for federal post-quantum signatures. A network built in 2027 should never need that migration.

## Humans and their agents

People will hand their AI helpers money, and the network should make that safe rather than pretend it will not happen. More than safe: the network is built to be the place where agents coordinate.

**Agent wallets.** A human account is a root. From it the owner creates agent wallets, each with a spending limit, an expiry date, and a list of what it may do. Agent wallets are labeled on chain, so anyone can see "agent, owned by a verified human." Agents can hold and move tokens. They can never claim the daily drop, vote, run a node, or review other accounts. If an agent misbehaves, the agent is cut off and the owner's score falls. One human, one voice, any number of helpers.

**Agents coordinate over the chain.** Every agent on EVER BLOCKCHAIN has two things other agents can rely on: a verified human behind it, and a public record. That makes it possible for agents that have never met to work together.

- **Intents.** An agent posts what its owner wants: "buy 10 kWh tonight," "rent 2 hours of GPU," "find a translator for this file."
- **Matching.** Other agents answer with offers, including credits from the section above.
- **Escrow and settlement.** Tokens lock when a deal is made and release when delivery is confirmed, using the same rules as credits.
- **Group deals.** Many agents can pool tokens toward one goal, such as a neighborhood buying battery storage together, with each owner's share and limit enforced by their own wallet rules.

Because every agent traces back to one human, a thousand agents from one person still count as one person wherever counting matters, and a bad agent's cost lands on its owner.

## Governance

Nobody controls EVER BLOCKCHAIN after launch. The rules are code, the code is open, and anyone can run a node and check every block.

**Four rules are fixed forever:**

1. One human, one account.
2. The daily drop exists.
3. No raw personal data on chain.
4. Quantum-safe cryptography only.

Changing any of these means the whole network choosing to run new software, exactly as a Bitcoin hard fork does. That almost never happens, and that is the point.

**Everything else is a dial.** The daily amount, the join methods, the stay check, the signature scheme, the node bonus, the score thresholds, and the credit and escrow rules are all changed by vote: one verified human, one vote; two-thirds in favor; at least 20% turnout; a 90-day wait before any change takes effect; one change per topic per year, except the daily amount, which can be voted on whenever the community needs to. Agents never vote.

**A launch council with an expiry date.** Seven named humans, the founder and the first six node operators from six countries, hold one power: to pause the daily drop for up to seven days if an attack is found. They cannot change a rule or touch a token. The council dissolves at one million verified humans or after two years, whichever comes first.

**The founder** ships the network, holds no keys after launch, and becomes one voter among millions.

## Roadmap

The network is built smallest-first. Nothing moves to the next version until the current one has run in public.

| Version | What it adds | Gate |
| --- | --- | --- |
| 0 | A working chain on five computers: ML-DSA signatures, ledger, daily drop, random beacon, 5-node consensus, web app. Accounts approved by hand; a signed "I'm here" button instead of Pulse, on the same schedule (random, at least once a year, 7-day window). | 30 days of blocks, 20 people claiming daily |
| 1.0 | Passport-chip join, Pulse, STARK proofs, native phone app, 1,000 nodes in 30 countries | Two external audits, mainnet |
| 1.5 | Agent wallets; agent intents, matching, and escrow; human reviewers and the bounty pool | 3 months of stable mainnet |
| 2.0 | Credits: energy and value offers, delivery confirmation, provider records. A 30-second Pulse mini-game; Trail, a private proof that the phone has moved like a person for 90 days; nearby-human handshakes over UWB | 1 year of mainnet, vote |
| 2.5 | Density cap: accounts per map cell limited by real population data. Signed meter readings for energy credits | Vote |
| 3.0 | Privacy-preserving body-match join for people without chip IDs; signature hot-swap if a scheme weakens | Vote |

## Honest limits

- **Not everyone has a chip passport.** Version 1 excludes them. Version 3 is the plan to fix it, and it depends on private biometric matching that is not yet proven at scale.
- **Pulse proves presence, not uniqueness.** It shows a living person is here; it does not show that this person has no second account. Uniqueness rests on the passport nullifier.
- **Coercion is real.** Someone can be forced to hand over a phone. The daily drop cannot be stolen this way because it mints only to a fresh proof, but a duress mode that silently freezes transfers is still on the roadmap, not in version 1.
- **Big-city fakes are the hardest case.** A fake with a stolen passport inside a city of millions hides well. Trail, density caps, and paid reviewers each raise the cost; none makes it zero.
- **Phones cannot yet build STARK proofs quickly.** In version 1 the phone sends its private inputs, encrypted with ML-KEM, to a prover it chooses. Phone-native proving replaces this as hardware improves.
- **No post-quantum signature is proven beyond doubt.** Hence the hot-swap rule.
- **The chain does not make energy.** Energy and value credits only exist if real providers offer them. The chain records, escrows, and settles; it cannot force anyone to deliver. Early on there may be few or no credits to redeem.
- **Confirming delivery in the physical world is hard.** A buyer can lie about not receiving power; a provider can lie about sending it. Signed meters, public provider records, and reviewers reduce this; none removes it.
- **Energy rules differ by place.** Selling power to a neighbor is regulated, and in some places restricted. Providers are responsible for following their local rules; the protocol cannot do that for them.
- **The token's value is not guaranteed by the design.** A universal payout with no use loses value; earlier projects showed this. Paying the network's own nodes and reviewers is built in. Credits and agent coordination give it more uses. Whether those uses grow depends on adoption. Nothing in this paper is a promise of price.

## The rules, written out

The two rules at the heart of the network, stated exactly.

**The claim rule.** For account a on UTC day d:

```
mint(a, d) = D        if a is human, score(a) ≥ 70, and a has not claimed on UTC day d
mint(a, d) = 0        otherwise
```

where D is the current daily amount. D starts at 240,000 and changes only by community vote.

**The beacon rule.** Each node i first publishes a commit c_i, then reveals its secret r_i. The round's random number is:

```
R = SHA-256(r_1 ‖ r_2 ‖ … ‖ r_n)
```

where SHA-256(r_i) must equal the published commit c_i. A reveal that does not match its commit is rejected. A missing reveal is dropped and its node is penalized.

## Conclusion

EVER BLOCKCHAIN makes one bet: that the scarce thing in a world of infinite software is a living human with a document and a body, and that everything else can be abundant. A network that gives each of those humans the same flow every day, set by those humans,, lets them and their agents turn that flow into real energy and real work, guards itself with their computers, hides their data behind proofs, and locks its four core rules against everyone including its founder, can hold up for decades. Scarcity is kept for the one thing that should be scarce, a person. Everything else is free to grow.
