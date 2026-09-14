Sparse Attention from scratch
Dense Attention-
In this each token is able to attend every other token.
Loss-
•	One of the biggest disadvantage of it high memory consumption.
•	Runtime grows rapidly with sequence length(O(n^2)) and is not efficient for very long sequences.
Though some of the advantages are-
There is no information loss.
It captures both local and global dependencies.
Sliding Window Attention-
In this token each token attends only to nearby tokens within a fixed window.
Loss-
•	Loses long-range dependencies
•	Distant tokens cannot directly communicate and global information may be missed.
Some of the advantages are-
•	It has the lowest memory usage among the implemented methods.
•	Fastest runtime for long sequences and efficient for capturing long context.
Block Sparse Attention-
In this tokens attend within blocks and selected additional connections.
Disadvantage-
•	It uses more memory than sliding window attention and slower than it.
•	Some long range relationships are still unavailable compared to dense attention.
Why global tokens matter disproportionately-
Global tokens can act as vital messengers that connect distant parts of the sequence. By introducing a small number of tokens in local-sparse attention, information from distant regions can be communicated through these tokens and shared across the entire sequence. Although global tokens constitute only a tiny portion they significantly improve information flow and quality of model and therefore this impact is disproportionately last compared to their cost.
Why Sparse Attention is worse-
Dense attention and block-sparse attention have access to considerably large amount of tokens and can acquire maximum information while sparse attention reduces computation and memory loss by removing many attention connections. It may produce worse results when long-range dependencies are important.


