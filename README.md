# GPT2 BPE Tokenizer

<div align="center">
<img src="./views/tokenizer.png" width="400">
</div>

## Abstract :

Re-implementation of the byte-pair-encoding algorithm on a toy text from an article to mint 50k tokens I have built this summer (2026).

We added 50k tokens to the 255 initial ASCII tokens + 1 special <|endoftext|> token to built up a 502556 long vocabulary in the goal of pre-training (no post-training specific tokens where implemented here for stuff like tool-calling, actions, ect..) 

The notebook also includes some discussion on the pros and cons that can arise from tokenization and the dataset selection specific to tokenization, discussing classical tokenization incidents such as the reason why early GPTs were bad with python (bad tokenization of tabs), the reason why they were bad with non-english natural language, or nonsensical tokens as the famous SolidGoldMagikarp token causing random semantics to be assign to a token that appears a lot in the tokenizer dataset but rarely in the actual training set of the GPT.

## Sources :

BPE paper : https://arxiv.org/pdf/2411.08671

Andrej Karpathy's tutorial on this build : https://www.youtube.com/watch?v=zduSFxRajkE

Tiktoken website to compare tokenizers : https://tiktokenizer.vercel.app/

Tiktoken library : https://github.com/openai/tiktoken
