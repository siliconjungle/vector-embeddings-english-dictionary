Another little trick to increase *guarantees* for outputs from llms.

This is a *reverse dictionary lookup*.

First I ask the llm to output a single word that best matches the description.

Then I check against a dictionary to see if that word exists.

If it does exist, return the word lowercased.

If it does not exist, get the results embedding & use nearest neighbour search to find the word which is closest to it.

<img width="537" alt="Screen Shot 2023-11-13 at 1 01 40 pm" src="https://github.com/siliconjungle/vector-embeddings-english-dictionary/assets/71357672/43c007d1-4f8e-42ee-9be7-bacb60aff65d">
