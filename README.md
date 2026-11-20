# word reasoning

Handoff. The working home for this idea is [poi-search](https://github.com/Azdwarf5Azdwarf/poi-search). The rule to carry there is the BMAP ceiling.

## The rule

BMAP is BM25 on a line of terminal blocks.

- The score is BM25. IDF sits inside it: a word weighs in inverse proportion to how many documents contain it, term frequency saturates, and document length is normalized.
- Each new block is placed behind the last and is 50% bigger. The first block is a person, 1.75 m: `h_n = 1.75 * 1.5^(n-1)`.
- The Earth–Moon mean distance is 384 400 km. Block 48 reaches 330 619 km. Block 49, placed behind that one and 50% bigger, reaches 495 928 km and hits the Moon.
- 49 is the last new block. After that, rank and reuse the blocks already in the line.

## Where the rest lives

[poi-search](https://github.com/Azdwarf5Azdwarf/poi-search) is the repo left unnamed by [poi-backend#17](https://github.com/Azdwarf5Azdwarf/poi-backend/issues/17). A request becomes a memory tree. An agent chooses the algorithm, then emits a Lisp Flavoured Erlang script that runs it on Mnesia. BM25 is one choice, beside a static chance product and an MCTS-style expansion. A fallback is still open.

Once the ceiling of 49 is written into poi-search, this repo can be removed. The same handoff is filed in both places so either copy is enough.

## A neighbouring note

The nine-response note is fork levels, in [fork-nivaer](https://github.com/Azdwarf5Azdwarf/fork-nivaer). Each agent gets about nine responses, then the thread folds and rotates. That is about levels of input and output in a thread. The written rule there says: after x iterations an agent pings its friends, a friend answers with a delta of what is happening, and the lookback stops at 3 days. The count is left as x. It may belong beside the ceiling of 49.

## Kernel

The lines below are the original note, left as written.

> lägg till markovian chains och fuzzy matching ska bygga min egen algortihm för "word reasoning"
>
> watch markovian chains by vertasium
>
> use BM25 and IDF for the vision reasoning

Issues #1–#6 are the longer notes behind that kernel. The open handoff issue is the active one.
