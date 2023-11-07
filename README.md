# vector-embeddings-english-dictionary

Vector embeddings for each word in `https://www.npmjs.com/package/word-list`.

It uses `text-embedding-ada-002` to do the embeddings.

You can use a Vector DB like `[chroma](https://www.trychroma.com/)` to handle search.
I would not recommend `https://github.com/Stevenic/vectra` for such a large embeddings list as it must all be in memory at once.

To compare two embeddings you can calculate their cosine similarity with libraries: `https://www.npmjs.com/package/compute-cosine-similarity`.

For more efficient comparisons you can use algorithms like these:
`https://www.npmjs.com/package/hnswlib-node`
`https://www.npmjs.com/package/hnswlib-wasm`

For visualising parts of the space you can use t-sne or related algorithms, e.g. `https://www.npmjs.com/package/@aidanconnelly/tsnejs`.

You can interpolate between different embedding spaces to find words which are *between* other words. You can get the mean of embedding spaces to try to isolate features.

There are also implementations of reversing embedding spaces in python:
https://github.com/jxmorris12/vec2text

https://colab.research.google.com/drive/1CF5Lr1bxoAFC_IPX5I0azu4X8UDz_zp-?usp=sharing#scrollTo=c74eDH1WG_nS
