# aslfr
I worked on this ASL Gesture Recognition Transformer Model from Summer 2024 all the way up to December 2024. (This is the simple version that doesn't use a feature extractor or squeezeformer/llama attention)

## Architecture

Basic encoder layer using mha and projection to feature dim, and then to a basic decoder using positional encodings and typical masked self-attention/cross-attention, and then projection with softmax activated linear layer to output

## Advanced Architecture

Originally, I wanted to use a feature extractor (not present in the code currently) and then feed it to a more complex encoder that utilized SqueezeFormer and LLaMA Attention with rotary embeddings but I scrapped the idea because I couldn't get the architecture to work with my data. I probably did some mistake in the processing feature, and dumbed down the architecture thinking that was the problem, but only later did I realize it was a preprocessing issue. I never bothered to go back to the originally planned architecture that would probably work much better.

## Metrics

I was also so lazy I didn't bother to implement levenshtein lmao but from inference i can see it's pretty accurate.
To avoid overfitting I had to implement a stupid amount of dropout (~0.5) in some places idk why tbh.

## Note

I didn't come up with this structure -- rather, I blended many other models/structures I saw and tried to learn from and combine them to understand transformers.
