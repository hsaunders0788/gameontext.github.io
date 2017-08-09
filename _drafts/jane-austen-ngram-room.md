---
layout: post
title: A Room for Jane Austen
summary: Exploration of ngrams and using ngram probabilities to construct sentences and paragraphs.
tags: [fun, profit, hadoop, java. scala]
author: ilan
---
## An Exploration of N-gram In Celebration Of Jane Austen
### The Conjecture
Over the last year I have been thinking, reading and learning about
`words in documents`. And what kind of information can be extracted
from `words in documents`. One interesting avenue of exploration is:
- The probabilities of two words appearing next to each other in a
particular order.
- The probability of three words appearing next to each other ...
- And so on and so forth.

Analysis of these probabilities have all sorts of interesting
implications; and, allow for fun experiments.

2017 is also a year for celebrating the novels of the great author
Jane Austen; as it has been 200 years since she passed on from this
world.

One way of participating in her celebration could be to create a Jane
Austen room, where using ngram probabilities from the words in her
novels, her corpus - one could interact with those probabilities in
various different ways using the game on protocols.

### Details that need to be Thought About
#### The Corpus
- [Apache Hadoop](http://hadoop.apache.org/) is the data cruncher.
- [sample-room-scala](https://github.com/gameontext/sample-room-scala) is the base template for the room.
- [Project Gutenberg](https://www.gutenberg.org/) is the data source for the `words in documents` i.e. the novels of Jane Austen.
- [The Book On Stuff Like This](https://web.stanford.edu/~jurafsky/slp3/) is The Book on Stuff Like This.

### The documents, their preprocessing and word tokenisation.
- [PERSUASION](http://onlinebooks.library.upenn.edu/webbin/gutbook/lookup?num=105) by Jane Austen
- [NORTHANGER ABBEY](http://onlinebooks.library.upenn.edu/webbin/gutbook/lookup?num=121) by Jane Austen
- [LOVE AND FREINDSHIP AND OTHER EARLY WORKS](http://onlinebooks.library.upenn.edu/webbin/gutbook/lookup?num=1212) by Jane Austen
- [PRIDE AND PREDUJICE](http://onlinebooks.library.upenn.edu/webbin/gutbook/lookup?num=1342) by Jane Austen
- [MANSFIELD PARK](http://onlinebooks.library.upenn.edu/webbin/gutbook/lookup?num=141) by Jane Austen
- [EMMA](http://onlinebooks.library.upenn.edu/webbin/gutbook/lookup?num=158) by Jane Austen
- [SENSE AND SENSIBILITY](http://onlinebooks.library.upenn.edu/webbin/gutbook/lookup?num=161) by Jane Austen
- [LADY SUSAN](http://onlinebooks.library.upenn.edu/webbin/gutbook/lookup?num=946) by Jane Austen

Before crunching the data some preprocessing and decisions on tokenisation of the
words in the document needs to be decided.
