# word reasoning

Handoff. The working home for this idea is [poi-search](https://github.com/Azdwarf5Azdwarf/poi-search). The rule to carry there is the BMAP ceiling.

## The rule

BMAP is BM25 on a board with a fixed size.

- The score is BM25. IDF sits inside it: a word weighs in inverse proportion to how many documents contain it, term frequency saturates, and document length is normalized.
- The first square is a person, 1.75 m. Each next square is 1.5 times the last: `h_n = 1.75 * 1.5^(n-1)`.
- The Earth–Moon mean distance is 384 400 km. Square 48 reaches 330 619 km. Square 49 reaches 495 928 km and passes the Moon.
- 49 is the last new square. After that, rank and reuse the squares already on the board.

## Where the rest lives

[poi-search](https://github.com/Azdwarf5Azdwarf/poi-search) is the repo left unnamed by [poi-backend#17](https://github.com/Azdwarf5Azdwarf/poi-backend/issues/17). A request becomes a memory tree. An agent chooses the algorithm, then emits a Lisp Flavoured Erlang script that runs it on Mnesia. BM25 is one choice, beside a static chance product and an MCTS-style expansion. A fallback is still open.

Once the ceiling of 49 is written into poi-search, this repo can be removed. The same handoff is filed in both places so either copy is enough.

## Kernel

The lines below are the original note, left as written.

> lägg till markovian chains och fuzzy matching ska bygga min egen algortihm för "word reasoning"
>
> watch markovian chains by vertasium
>
> use BM25 and IDF for the vision reasoning

Issues #1–#6 are the longer notes behind that kernel. The open handoff issue is the active one.
