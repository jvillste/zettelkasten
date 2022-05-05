To find an optimal keyboard layout for typing a given text by a given person one would have to first measure which finger movements are the most efficient and then find a layout that uses the most efficient finger movements for the given text.

To measure the efficiency of each finger movement one could make the person type the text and measure the time it takes to write each digram in the text; assuming the person knows the used keyboard layout so well that he does not have to search for the keys. The typed text could be an excerpt of the whole text containing all of the most common digrams of the whole text. The whole text could be for example the contents of the english wikipedia.

The result would be a list of key pairs corresponding the digrams in the text and the average time it took to type them.

One could then calculate the efficiency of a given layout by multiplying each digrams propability by the time it took to type the corresponding key pair. The smaller this number is, the more efficient the layout is.

Calculating the efficiency of every possible layout is not possible because the number of permutations in the latin alphabet is 26! = 4.0E26. Assuming that calculating the efficiency of one layout took 0.1 milliseconds, it would take 1.3E15 years to rate them all.

Finding the optimal layout could be an intearctive proces between a computer and a human. The human could suggest a layout and the computer could then search for a local optimum by swaping key pairs until no more efficient layout is found. Then the computer could present an analysis of which are the most common and slowest key pairs used in the layout and the human could then try to invent a better layout.