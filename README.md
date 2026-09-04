# word reasoning

## Karnan

> lägg till markovian chains och fuzzy matching ska bygga min egen algortihm för "word reasoning"
>
> watch markovian chains by vertasium
>
> use BM25 and IDF for the vision reasoning

Ovanstaende ar oredigerat och star som det star. Allt under den har raden ar
stallning byggd runt det — terminologi och referenser, inte omskrivningar.

## Delarna

**Markovkedja (Markov chain)** — nasta ord valjs bara utifran de n foregaende
orden, inget minne langre bak an sa. Billig att bygga ur en textmangd, och den
gor sannolikheterna synliga i stallet for att gomma dem i vikter.

**Luddig matchning (fuzzy matching)** — matcha ord som nastan stammer.
Redigeringsavstand (Levenshtein) for stavfel, trigram eller soundex for
uttalslikhet. Behovs sa att kedjan inte tappar en overgang bara for att
ordet var felstavat.

**BM25** — rankningsfunktion for hur val ett dokument svarar mot en fraga.
Bygger pa termfrekvens med matthet (ett ord som redan forekommit tio ganger
tillfor lite pa den elfte) plus dokumentlangdsnormalisering.

**IDF (inverse document frequency)** — vikten av ett ord ar omvant mot hur
manga dokument det finns i. "och" vager nastan noll, "markovkedja" tungt.
Sitter inuti BM25 men ar anvandbar for sig.

## Lage

Ingenting byggt an. Se issues for vad som star pa tur.
