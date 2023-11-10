# Interpolation

Since the data set is *very* sparse as it only has words and no sentences, interpolation doesn't give very interesting results.

e.g. interpolating between `sadness` and `happiness` will only give you `sadness` or `happiness`, there aren't any words between.
I haven't tested all cases but it seems like the probability is likely that this is the case for all of the elements.

I also tested this with the `centroid` of many elements and it had a similar result. The only difference being that the element which is selected is the one that is closest to all terms.

Something that needs further exploration is to *add* the difference between two elements in a direction. e.g. add the difference between `sadness -> happiness` to find a new word `happiness -> ??`.