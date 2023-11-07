# vector-embeddings-english-dictionary

Vector embeddings for each word in [word list](https://www.npmjs.com/package/word-list).

It uses `text-embedding-ada-002` from [Open AI](https://platform.openai.com/docs/guides/embeddings/what-are-embeddings) to do the embeddings.

## Comparing embeddings

You can use a Vector DB like [chroma](https://www.trychroma.com/) to handle search.

I would not recommend [vectra](https://github.com/Stevenic/vectra) for such a large embeddings list as it must all be in memory at once.

To compare two embeddings you can calculate their cosine similarity with libraries: [compute cosine similarity](https://www.npmjs.com/package/compute-cosine-similarity).

For more efficient comparisons you can use algorithms like these:

[hnswlib-node](https://www.npmjs.com/package/hnswlib-node)

[hnswlib-wasm](https://www.npmjs.com/package/hnswlib-wasm)

## Visualisation

For visualising parts of the space you can use t-sne or related algorithms, e.g.

[t-sne js](https://www.npmjs.com/package/@aidanconnelly/tsnejs).

## Interpolation

You can interpolate between different embedding spaces to find words which are *between* other words. You can get the mean of embedding spaces to try to isolate features.

## Reverse embeddings

There are also implementations of reversing embedding spaces in python:

[vec2text](https://github.com/jxmorris12/vec2text)

[Contra](https://colab.research.google.com/drive/1CF5Lr1bxoAFC_IPX5I0azu4X8UDz_zp-?usp=sharing#scrollTo=c74eDH1WG_nS)

## Data structure

There are a series of embeddings files in `/embeddings` which are in order & contain an array of objects in the following format:

```
[
  { word: '', embedding: [] },
]
```

## Additional metadata

[wordpos](https://github.com/moos/wordpos) can be used to attach metadata such as `noun, verb, adjective, adverb, synonyms, definition` etc.

In the `/metadata` folder is noun, verb, adjective, adverbs & the word's lookup. Not all words are known by wordpos.

I think some interesting things can be done by filtering words based on their properties.
