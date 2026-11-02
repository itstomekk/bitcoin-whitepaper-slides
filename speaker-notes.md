# Whitepaper Day: script and speaker notes

Generated from `presentation.html` (v5, 30 slides). Slide numbers match the deck. Keys: arrows move, N notes panel, P presenter window, M slide list, F fullscreen, Whitepaper button (top bar) opens the original paper with zoom.

Storyline: **Part 1** the problem of money (gold, bank money, how the referee grew, digital copies) · **Part 2** attempts at digital money and the pieces invented before 2008 · **Part 3** the email, five sentences from the paper, then section by section (hash, timestamp, proof-of-work, network, attacks, who decides, incentive, outputs, race) · then paper vs code and the dials.

Keywords that return all evening: SALABILITY, SCARCITY, VERIFIABILITY, OWNERSHIP, NO DOUBLE SPEND, PRIVACY, NO REFEREE.


## 1. Title

**Say:** Welcome to Cargo’s Dockside. We are going to read nine pages together, and by the end you will be able to explain every one of them to someone else.

- The paper was posted to a cryptography mailing list on 31 October 2008. Today is its anniversary.
- Order of the talk: first the problem of money (gold, bank money, digital copies), then the pieces people invented before 2008, then the email, then the paper section by section, then what the paper does NOT say.
- Keys for you: arrows = move, N = notes under the slide, P = presenter window, M = slide list, F = fullscreen, the Whitepaper button in the top bar opens the original pages with zoom.


## 2. Money: gold

**Say:** Let’s start with money itself, with no Bitcoin at all. Economists ask three things. Can it travel (salability across space)? Can you pay a small and a large amount (salability across scale)? Does it hold its value (salability across time)? Add scarcity, easy verification, and provable ownership.

- Gold scores well on time, scarcity and ownership (whoever holds it owns it). It scores badly on space (heavy, risky to move) and scale (hard to split).
- Introduce these row labels now; we keep returning to them: SALABILITY, SCARCITY, VERIFIABILITY, OWNERSHIP, NO DOUBLE SPEND, PRIVACY, NO REFEREE.
- Tap cells on the slide to read the reason behind each mark. The marks are a judgement call, not data: say so if challenged.
- Gold has no double-spending problem. A physical thing is in one place. That is the key property digital money loses.


## 3. Money: bank money

**Say:** Bank money (fiat) is excellent at travel and scale: seconds, any amount. And a physical coin is never in two places, so what stops a bank balance being spent twice? The bank. It keeps the only ledger, so it is the referee. That is a trusted third party.

- The third party is useful and also costly. It sees everything (privacy gone). It can say no or freeze you (ownership is a claim on the bank, not the thing itself). It decides how much money exists (scarcity is its decision).
- Trust is not bad by itself. The point is that the whole system depends on one party being honest and staying in business.
- Fiat holds value less well across time because the issuer can create more (inflation). Keep this neutral; it is a trade-off, not a verdict.


## 4. Digital: the copy problem

**Say:** A photo can be copied freely: send it and you both have it. If money behaved like that it would be worth nothing. This is double spending: the same coin paid twice, with two perfectly valid signatures.

- Press both buttons. Both Bob and Carol receive something that looks valid. Nothing in the data itself tells them which one is the real one.
- Signatures prove WHO approved a payment. They do not prove that NOTHING EARLIER exists.
- Digital cash was not impossible: David Chaum’s DigiCash existed. What was missing was digital cash WITHOUT a company in the middle.


## 5. The old fix: a referee

**Say:** The paper opens with the cost of the referee. Banks cannot avoid mediating disputes, so payments can be reversed. Reversal means everyone must be wary: merchants ask customers for more data, a percentage of fraud is accepted as unavoidable, and small casual payments become impractical.

- He notes that physical cash avoids all this, in person. What nobody had was cash-like payment over a communication channel.
- Your reading was correct: cost AND risk, both avoidable with cash.
- Fair caveat: Bitcoin has its own costs (fees, confirmation waits, energy). Say so now, return to it at the end.
- Ask: which of these have you paid personally? Chargeback, frozen account, fee on a tiny payment?


## 6. Referees through history

**Say:** Nobody invented the referee to be annoying. Each step solved a real problem of the step before. Gold in the hand needs nobody, but it only works in person. Receipts let you pay across town, and now someone must keep the gold safe. Banks and bank notes let a whole country pay each other, and now one ledger decides. Cards and online payments extend the same referee to the internet. Satoshi’s sentence at the bottom is the problem statement of the whole paper.

- Tap each step and read the two lines: who the referee is, and what you give up. The pattern repeats every time.
- Dates to be comfortable with: goldsmiths’ receipts in 17th-century England; the Bank of England in 1694; 15 August 1971, when the US ended the convertibility of the dollar into gold; the first general-purpose charge card, Diners Club, in 1950.
- The history is simplified on purpose. Real systems mixed these stages for centuries (coins, notes and bank money lived side by side).
- Section 1 of the paper lists the costs of the referee: disputes, reversibility, merchants distrusting customers, accepted fraud, no small payments. Cash avoids them only in person.
- Ask: which of these referees have you personally depended on this week?


## 7. The goal: every row ✓

**Say:** This is the whole story in one picture. Gold ticks privacy and needs no referee, but cannot travel. Bank money travels, but needs a referee and watches you. The wish is digital cash that ticks every row. Notice the last three rows: NO DOUBLE SPEND, PRIVACY, NO REFEREE. They are the ones that fight each other.

- Satoshi’s own words for the goal are on the right (§1): cryptographic proof instead of trust.
- Next slide: the inventions people made between 1976 and 1998, each aimed at a row of this table.


## 8. Digital money attempts

**Say:** Before Satoshi, people did build digital money. It worked technically. What failed was the business around it: the money lived and died with one company. DigiCash had private digital coins and bank pilots, and it went bankrupt. CyberCash tried wallets and micropayments, and it went bankrupt. E-gold had real traction, and its owners ended up pleading guilty. The last card, b-money and Bit Gold, wanted no company at all, but nobody could say how strangers would agree on one history. That is the gap the paper fills.

- Sources (checked 31 Oct 2026): New York Times, 28 Nov 1998 and American Banker on DigiCash’s bankruptcy; Forbes, 1 Nov 1999 on the Mercantile Bank trial (about 5,000 customers, accounts totalling about $100,000) and on CyberCash dropping CyberCoin; CyberCash filed Chapter 11 on 11 March 2001 (founded August 1994); US Department of Justice press release #08-635 of 21 July 2008 on E-Gold.
- Sources disagree on DigiCash’s start (1989 to 1990). The slide says 1990, from a European Commission article and American Banker (“eight-year-old Digicash”).
- Why DigiCash failed is debated: complexity, management problems, too few merchants and banks that wanted customer data. Do not reduce it to one cause.
- The e-gold dates are approximate at the start; the 2008 plea is the verified date. Sentencing and what happened to the service afterwards is not on the slide.
- b-money (Wei Dai) is reference [1] in the paper. Bit Gold (Nick Szabo) is not cited by the paper.
- Bridge to the next slide: now meet the pieces people invented, each aimed at one row of the table.


## 9. Before 2008: the pieces

**Say:** Here is the reading order of the history. Each invention solved one row of the table. Public-key signatures: OWNERSHIP without a central host. Merkle trees: VERIFIABILITY of a big list. Blind signatures: PRIVACY. DigiCash: all of that as a product, with a company in the middle. Timestamping: ORDER. Hashcash: SCARCITY through work. b-money: money made by work, with the agreement question left open.

- The pattern to point out: every piece solves one thing and leaves one thing missing. Open each event and read the STILL MISSING line.
- Only four of these are cited in the paper: b-money [1], timestamping [2–5], Hashcash [6], Merkle [7].
- Blind signatures and DigiCash are NOT cited. They explain why digital cash had been tried, not what Satoshi used.
- Dates: Diffie–Hellman 1976, RSA 1977, Merkle’s paper 1980, Chaum’s blind signatures 1982, DigiCash 1989 (bankrupt 1998), Haber and Stornetta 1991, Hashcash 1997, b-money 1998.


## 10. 31 Oct 2008: the email

**Say:** On 31 October 2008, an author using the name Satoshi Nakamoto sent a short email to a mailing list of cryptographers. This is the real text. Read the five properties: they are exactly our rows. No mint. No double spending. Participants can be anonymous. New coins from work.

- Verified: Metzdowd cryptography list, “Bitcoin P2P e-cash paper”, Fri Oct 31 14:10:00 EDT 2008 (18:10 UTC). The same email carried the abstract and a link to the PDF.
- The email’s abstract differs slightly from the final PDF. The email says “As long as honest nodes control the most CPU power”. The PDF says “As long as a majority of CPU power is controlled by nodes that are not cooperating to attack the network”. We use the PDF text on the next slide.
- Early replies on the list raised scaling and trust objections. Worth telling the room: it was not welcomed as obvious.
- Why a cryptography list? That is where people who had tried digital cash (and failed) were reading.


## 11. Five sentences from the text

**Say:** These five sentences come from the body of the paper, not from the abstract. Tap a number and the real page appears with the sentence highlighted. One: the goal, proof instead of trust. Two: why everyone has to see all payments. Three: why history is expensive to rewrite. Four: how the network decides, by the longest chain. Five: why attackers are better off honest. The rest of the paper explains how these five work.

- Read each highlighted sentence aloud, then say the short line in your own words.
- 1 is on page 1 (§1), 2 on page 2 (§2), 3 and 4 on page 3 (§4), 5 on page 4 (§6). The button opens that page in the zoom viewer.
- Sentence 3 includes “catch up with and surpass the work of the honest nodes”: the attacker must not only redo the work, he must be faster than everyone else.
- Sentence 4: “one-CPU-one-vote” is in the line just before it. The vote is not people or IP addresses, it is work.
- Sentence 5 is Satoshi’s incentive argument. It is an argument about profit, not a proof. It assumes the attacker cares about the value of his coins.
- The abstract is still worth re-reading at the end; it is on page 1 in the whitepaper viewer.


## 12. The paper’s own pictures

**Say:** While you read a chapter, this is the picture that belongs to it. Tap the chapter tab. These are the paper’s own figures, cropped from the PDF, so what you show is what the room can find in the document. Section 6 has no figure in the paper, so we drew one.

- §2 page 2: the chain of three transactions. Owner 1 signs the hash of the previous transaction plus Owner 2’s public key; Owner 2 does the same for Owner 3.
- §3 page 2: timestamp server. §4 page 3: block with previous hash, nonce and transactions. §7 page 4: Merkle tree and pruning. §8 page 5: longest chain and the Merkle branch. §9 page 5: inputs and outputs. §10 page 6: privacy models.
- §5 (network steps) and §11 (calculations) have no figures; they have the live simulations on slides 18 and 23.
- The same pages can be opened full-size with zoom from the Whitepaper button in the top bar.


## 13. Why a chain, not a token?

**Say:** A digital token can be copied, so it proves nothing by itself. Satoshi defines the coin by its history: each owner signs the coin over to the next. Press “Pass it on” and watch the chain grow. Every arrow is a real digital signature over the previous transaction and the next owner’s public key. Anyone can check all of them. Now press the red button: an earlier owner signs the same coin again to someone else. Both chains verify perfectly. The signatures cannot say which one counts. That is exactly the problem of section 2.

- The signatures here are real secp256k1 signatures made in your browser. Bitcoin itself uses a similar scheme, with extra detail the paper does not describe.
- “Verify the chain” checks every link from the first owner onwards.
- In real Bitcoin you do not carry the chain with you. Every node keeps the shared record and checks that an output is still unspent (UTXO is a later name).
- Bridge: the chain proves who gave it to me. Only an agreed order proves which branch counts.


## 14. Three tools

**Say:** Three tools, no more. A hash turns any text into a fixed-length fingerprint. Type something, then change one letter and watch how most of the 64 characters change. You cannot go backwards from fingerprint to text, you can only guess and check. A signature proves a key owner approved a message. A timestamp proves data existed by a certain time.

- The lab runs a real SHA-256 (the function the paper names). Check: SHA-256 of “abc” starts with ba7816bf.
- Do not explain SHA-256 internally. It is “a machine that turns any text into 64 hex characters, always the same for the same text”.
- Bitcoin actually hashes twice in many places; the paper just says SHA-256.


## 15. How 5 becomes 239 (hash math)

**Say:** Where does the 239 come from? From arithmetic, nothing magic. Tab one is a toy version you can follow with a calculator: split the number into bytes, XOR, multiply and add, then take the remainder after dividing by 256, rotate the bits, fold the ends together. The key step is the remainder. It forgets how many times 256 fitted, and that information is gone for good. Tab two is the real SHA-256 for the same number: the same kinds of operations, 64 rounds, on 32-bit words. Slide the bar and watch the eight registers change. At the end the first byte of the real hash for 5 is 239. Tab three shows what going backwards costs.

- The toy is not SHA-256. It only teaches the ingredients: XOR, multiply, add, “mod”, rotate. Say that out loud so nobody thinks Bitcoin uses it.
- Real SHA-256 of the text “5” starts with ef, and ef in hex is 239 (14 × 16 + 15). The tab shows the full 64 rounds computed live in your browser, with the same constants the standard uses (square and cube roots of the first primes).
- “mod 2³²” in the real function is the same idea as “mod 256” in the toy: add, then throw away anything that does not fit.
- Why it is one-way: each round mixes the words and throws away overflow, 64 times over. There is no known shortcut from the output to the input. The only method is to guess and check.
- Why that matters for Bitcoin: proof-of-work (§4) uses exactly this lopsidedness. Finding a number whose hash starts with zeros takes many guesses. Checking one takes a single hash.
- Here the “number” is turned into its text form (“5”) before hashing. Bitcoin hashes bytes of block headers and applies SHA-256 twice, but the principle is identical.


## 16. §3: timestamp

**Say:** Timestamping answers one question: did this document exist at that time, and has it changed since? You never publish the document. You publish only its fingerprint, together with the time and the fingerprint of the previous stamp. Each stamp therefore contains the one before it. Change any old stamp and every later one stops fitting.

- Press “Stamp it now” with your own sentence. A new card appears with the real time, the document’s hash, the previous stamp’s hash, and the new stamp hash.
- Check a document: pick a stamp and type the original text. ✔. Change one letter. ✗. The stamp proves existence and integrity, not who wrote it.
- Tamper: edit the time or hash on an old card. Its stamp hash changes, the link to the next card is cut (✂), and everything after it turns red. That is why the paper says each timestamp reinforces the ones before.
- The weak point to mention: someone must run the clock and decide who adds the next stamp. That is the job Bitcoin gives to proof-of-work on the next slide.
- Real world examples: Haber and Stornetta (1991) published their hashes weekly in the New York Times. The Bitcoin genesis block carries a Times headline.
- Paper §3, page 2, with Figure “Timestamp server”: see slide 12.


## 17. §4: Hashcash, data + nonce

**Say:** This is Adam Back’s Hashcash, the idea Satoshi names in section 4. You have some data, for example an email header. You glue a number to it, the nonce, and hash the lot. If the hash does not start with enough zeros, add one to the nonce and hash again. Keep going. When it works you have a stamp that proves you did the work, and anybody can check it with a single hash.

- Start with “Step”, one click at a time, so the room sees the loop: data + nonce → SHA-256 → check zeros → ✗ → nonce + 1.
- Then Fast. With 3 zeros you need about 4,000 tries (16 × 16 × 16), with 5 zeros about a million.
- Press “Receiver checks”: one hash is enough. Cheap to check, expensive to make. This asymmetry is the whole trick.
- The strip of past runs shows luck: the average is 16^zeros, but one run can be far faster or slower.
- Zeros here are hexadecimal digits (each is 4 bits). Bitcoin counts bits against a target, same idea.
- Hashcash was meant to make spam expensive. Satoshi reuses it so that adding a block of payments is expensive, which makes rewriting history expensive. Next slide: the same loop on a block of payments.


## 18. §4: be a miner (slow motion)

**Say:** A block holds the payments, the fingerprint of the previous block, and a number the miner can change, the nonce. The miner hashes all of that. If the fingerprint does not start with enough zeros, change the nonce and try again. And again. Nobody can shortcut it: the only way is to guess. When a guess works, the block is valid and anyone can check it with one hash.

- Press Start guessing at 4 per second and let the room watch the nonce count up. Then slide the zeros to 3 or 4 and use “as fast as possible”.
- Each extra zero makes it 16 times harder: 1 zero is about 16 guesses, 4 zeros about 65,000.
- Tab 2, Rewrite history: edit any payment. Its fingerprint changes, the next block’s link breaks, then all later blocks. “Recalculate the chain” re-mines every broken block and shows the cost. The counter shows how much more the honest network added in the meantime.
- Zeros are counted in hexadecimal digits here. Real Bitcoin counts bits, and compares the hash with a 256-bit target, but the idea is the same.
- This is a teaching simulation: real mining uses a double SHA-256 on an 80-byte header at hundreds of exahashes per second. The paper’s “one-CPU-one-vote” is §4.


## 19. §5: from payment to final

**Say:** Follow Alice’s payment, one button at a time. She builds it from a coin she owns (an unspent output) and signs it with her private key. The signature is real, on the same curve Bitcoin uses. She tells one node, and every node checks it and passes it on. A miner collects it into a block, finds the proof-of-work, announces the block, every node re-checks everything, and then more blocks pile on top. After about six, an attacker with less than half the power has almost no chance.

- This follows the six steps in §5 of the paper. The step badge at the bottom of the panel shows which paper step you are on.
- Tick “double spend” on step 1: Alice also pays Carol with the same coin. Different nodes hear different versions first. The miner picks the one it heard first. Every node drops the other one, because its coin is already spent. Carol never gets paid.
- Try editing a payment in a block at the bottom, or lower the zeros and “Repair the chain”. The chain tells you which block no longer fits.
- Details the paper leaves out: the waiting room is called the mempool, and exact validity rules live in the code. Here: signature valid, coin unspent, outputs not above inputs, nothing conflicting.


## 20. §5: attacks that fail

**Say:** Three kinds of cheating, three different answers. A fake payment: every node checks it and throws it away, so it never even reaches a miner. A dishonest miner: he can spend real electricity on a block with a rule broken inside, and every honest node simply ignores it. A secret chain: the only attack the paper takes seriously. It needs more than half of the power to be certain, and a shop that waits for more confirmations makes it less likely.

- Tab 1: pick a cheat and see which of the five checks fails. “Mallory signs” uses a real signature from a different key; it fails against Alice’s public key. “Alice signs” is the control: it passes.
- Tab 2: the miner really does the proof-of-work. Raise the reward above 50 plus fees and the block is rejected. Everybody keeps mining on the last good block, and the cheater’s work is wasted.
- Tab 3: block by block version of the §11 race. The attacker mines a secret chain. If it ever gets longer than the public chain, he publishes it and nodes follow it, so the shop’s payment disappears. Use “20 attacks” to compare with the paper’s formula.
- What a majority of the power can and cannot do: reverse its own recent payments, delay or leave out other people’s payments. It cannot create coins out of thin air, spend coins it does not own, or change rules that nodes enforce.
- The reward rule used here (50 plus fees) matches the first era of Bitcoin’s rules; it is not in the paper.


## 21. §5: who decides the rules (the stack)

**Say:** The paper says nodes vote with their CPU power. In practice four different groups hold four different kinds of power. Software writers write the rules down. Nodes check them. Miners put payments in order. And in the end people and businesses decide which of those rules they call Bitcoin. Look at where the concentration really is: software and miners are the most concentrated layers, nodes are much more spread out.

- Numbers (31 Oct 2026): pools, last 7 days: Foundry USA 26.4%, AntPool 20.0%, F2Pool 17.0%, ViaBTC 9.0%, Luxor 5.3%, SpiderPool 4.7%, MARA 4.4%, SECPOOL 4.3%, OCEAN 3.6%, others 5.3%. Source: firsthandbitcoin.com, which estimates hashrate share from blocks found. Short windows are noisy.
- Nodes: 18,236 public nodes, of which 16,339 Bitcoin Core (89.6%), 1,872 Bitcoin Knots (10.3%), the rest under 0.1%. Source: coin.dance.
- A pool is a coordinator. The hash power belongs to many owners who can move. A big pool is a risk, not a proof of control.
- Knots vs Core: same consensus rules, different relay policy. A difference in relay policy is not a fork.
- Not on the slide, but part of the real stack: chip makers, electricity, exchanges, wallets, and developers who can merge code. Say them aloud if the room asks; I did not find reliable current numbers for those layers.
- Historical examples of the “people” layer: 15 Aug 2010 overflow bug (about 184 billion coins) was fixed within hours and the buggy chain abandoned; 1 Aug 2017 Bitcoin Cash split.
- Interpretation (mine): Bitcoin is a rule set that enough people keep choosing.


## 22. Section 6: incentive

**Say:** Two jobs with one mechanism. First: pay the people who spend electricity securing the chain. Second: issue the money, since there is no central bank. The first transaction in each block creates new coins for the block’s creator. Later, fees can replace new coins.

- Gold analogy from the paper: a constant amount of new coins, like gold miners adding gold to circulation, here costing CPU time and electricity.
- The attacker’s dilemma: someone with more power than everyone else could steal back his own payments, or simply mine new coins. Satoshi expects the honest path to pay more, because attacking undermines the validity of his own wealth.
- Why do nodes want the longest chain? A miner’s reward counts only if his block stays in the chain others accept.
- Careful: the paper says “constant amount” and “a predetermined number of coins”. It has no 21 million, no halving. See the last part of the talk.


## 23. §9: inputs, outputs, fee

**Say:** Think of cash. You owe 3 and you only have a 5 note. You do not tear it. You hand over the whole note and get 2 back. A transaction works the same way: the inputs are whole coins you spend, the outputs are the new coins created: one for the person you pay, one for your change. The little gap between what goes in and what comes out is the fee for the miner.

- Preset “Split”: pay 3 with the 5 coin. Outputs: 3 to Bob, 1.9 back to Alice, 0.1 fee. The ribbons show where the value goes.
- Preset “Combine”: pay 7.4 with 5 + 2 + 1. Three inputs become one transaction.
- Preset “Too small”: pay 3 with the 2 coin. The inputs cannot cover payment plus fee, so the transaction is invalid. Add another coin.
- Rule to say aloud: inputs = outputs + fee. Nothing is created or destroyed. The fee is not written anywhere; it is simply the difference.
- Paper §9 and Figure “Transaction” (slide 12, tab §9). The paper says value is combined or split, normally one input or several, and at most two outputs: payment and change.
- Next slide shows several transactions in a row: outputs of one become inputs of the next.


## 24. §9: change, like cash (UTXO chain)

**Say:** This is how value really moves. A payment does not change a balance. It destroys some coins, the inputs, and creates new ones, the outputs. What you do not send comes back to you as change, like handing a note to a cashier and getting coins back. The lines show exactly which output became which input. Click or hover a coin to light up its whole family tree, all the way back to the reward that created it.

- The slide opens with three payments already done: Alice receives a reward of 50 (TX 0). She pays Bob 20 and keeps 29.9 as change, 0.1 is the fee (TX 1). She pays Bob 15 more (TX 2). Bob now has two coins and must combine both to pay Carol 30 (TX 3). Press “Next example” for Carol → Dave 12 (TX 4).
- Try your own: pick who pays whom and how much, press Send. The wallet picks the coins itself, largest first. Hover a payment card to light up its whole family: backwards to the reward, forwards to what the money became.
- Check the line at the bottom: total ever created = coins still unspent + fees paid. Nothing appears or disappears.
- Every output can be spent only once. That one rule, checked by every node, is “no double spending” in practice.
- The word UTXO (unspent transaction output) is not in the paper. The paper describes value being combined and split (§9). A wallet balance is just the sum of the unspent outputs it can sign for.
- Fees are not written anywhere: they are inputs minus outputs.


## 25. §11: the race

**Say:** The shop sells something and has to decide how many blocks to wait before shipping. The honest network (green) keeps finding blocks. An attacker with a share of the power secretly builds a rival chain (red). The shop waits until the honest chain is z blocks long. The attacker wins only if the red line catches up. Try 30% with 3 blocks: sometimes. Try 10% with 6: practically never.

- Run one race several times, then run 20,000 and compare with the paper’s formula (printed next to it). They agree within noise.
- At 50% or more the attacker always catches up. That is why sentence 4 of the abstract is a condition, not a detail.
- Paper numbers to quote: q = 0.1, z = 5 gives 0.09%. q = 0.3, z = 20 gives 0.25%.
- The paper’s model: the attacker only tries to undo his own recent payment. He cannot create coins out of nothing or take other people’s coins, because he cannot forge signatures. This is the only security argument in the paper.


## 26. Paper vs code

**Say:** Where is the 21 million? Not in the paper, and no pages are missing. The paper is the blueprint: the mechanism and why it is secure. The code is the building: exact numbers, exact rules, built in 2009 and 2010. The same blueprint could have been built with other numbers, and the dials slide lets you try.

- Design means: the idea and the security argument. Implementation means: working code with exact numbers. Bitcoin as it runs today is defined by the code and by the people who choose to run it, not by the PDF.
- Paper word counts: blockchain 0, wallet 0, UTXO 0, halving 0, mempool 0, “21” 0. “Mining” once, “miner” once, “10 minutes” once as an example in §7.
- What the paper does say about supply: “a constant amount of new coins” (§6), and later “a predetermined number of coins”.
- How to name the paper: a protocol design or consensus architecture.
- The genesis block (3 Jan 2009) carries the headline “The Times 03/Jan/2009 Chancellor on brink of second bailout for banks”.
- The motive for the 1 MB limit is not stated in the commits. Do not present a reason as fact.


## 27. Turn the dials

**Say:** Same design, different dials. Reward, halving, block time and block size are choices made in the software, not in the paper. Three tabs show what they change. Money supply: how many coins exist, the reward in each era, and the yearly inflation. Speed: how many payments per second fit, how long you wait for safety, and how few payments per person that adds up to. Disk and bandwidth: how big a full node gets, how much it downloads each month, and how long a new node takes to sync.

- Defaults are Bitcoin’s: 50, every 210,000 blocks, 10 minutes, 1 MB, full blocks, 250-byte payments, 10 years. Supply comes out near 21 million (exactly 20,999,999.9769 in integer arithmetic).
- Try block size 32 MB with full blocks: payments per second jump, and a full node grows by more than a terabyte a year. Bigger blocks mean more payments and fewer people able to run a node. That is the block size debate in one picture.
- Try 1-minute blocks: the same total supply, but the whole schedule runs ten times faster. Halving is counted in blocks, not years.
- Try “never” halving: the supply never stops growing and the yearly inflation falls only slowly.
- Speed tab, middle chart: waiting more minutes lowers the attacker’s chance. It uses the paper’s §11 formula. It does not model that very short blocks collide more often.
- Sync time is download only, at an ideal constant speed. Real nodes also spend time verifying.
- The disk numbers ignore the extra indexes real nodes keep. Treat them as the order of magnitude. The dials are a teaching toy, not a forecast.


## 28. Why these numbers?

**Say:** Can we find reasons for the numbers the paper leaves out? Some, yes. The cap and halving: Satoshi explained that without halving there would always need to be some minimum reward, so no finite limit. The retarget period and the four-year halving were stated in a 2009 post. The ten-minute block time is only an example in Section 7. The block size limit appeared in 2010 and the commits do not explain it.

- Sources used: Satoshi’s bitcointalk post of 14 Feb 2010 (“What’s with this odd generation?”); Satoshi’s P2P Foundation post (2009); BitcoinWiki “Scalability FAQ” on the block size history (15 July 2010 mining limit of 990,000 bytes; 7 Sept 2010 consensus limit of 1,000,000 bytes after block 79,400). Also Satoshi, 5 Aug 2010, on large blocks being fine later.
- [verify] exact date of the P2P Foundation post; the usual “anti-spam” explanation for the block size limit is a commonly repeated reading, not stated in the commits.
- Ten-minute blocks: my inference. Do not present it as Satoshi’s stated reason.
- Why leave these out of the paper? Interpretation: the paper argues security of a mechanism. Parameters can be tuned without changing the argument, so they sat in the implementation.


## 29. So what is Bitcoin?

**Say:** So what is Bitcoin? Digital cash with no issuer, kept honest by a shared ledger that thousands of computers check, where ownership is a key and security is paid for with work. And the rulebook is software that people choose to run. Look at the table: Bitcoin ticks the rows gold and bank money could not, with real trade-offs: it is volatile, public payments are only pseudonymous, and lose the key and you lose the coins.

- If the paper feels less revolutionary than you expected: that is a fair reaction. Every ingredient was old (slide 7). What was new is how they fit: agreement between anonymous strangers, kept honest by incentives paid by the system itself.
- Papers do not change the world, running systems do. The software was released in January 2009 and kept running.
- Fair caveats to say out loud: fees and waiting for confirmations, energy use, volatility, privacy is pseudonymous not anonymous, and a lost key cannot be reset.
- The table marks are my judgement. Defend them with the reason on each cell.


## 30. Read it yourself

**Say:** Here are all nine pages. It is shorter than most emails people send each day. Scroll the mouse wheel to zoom into the spot under the cursor, drag to move, double-click to fit the page, and use the thumbnails on the left. The same viewer opens from the Whitepaper button in the top bar at any time.

- Good closing move: read the abstract aloud one more time and ask which phrases they can now explain.
- The original PDF: bitcoin.org/bitcoin.pdf (link inside the viewer).
