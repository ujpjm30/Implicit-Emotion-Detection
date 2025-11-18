## Implicit Emotion Classification with K-BERT + SenticNet

This project improves K-BERT’s ability to detect implicit emotions by redesigning how external sentiment knowledge is injected into the model.

### What I Built
- Integrated **SenticNet** into the K-BERT structure using a sentence-tree approach with **soft-position embeddings** and a **visible matrix** to reduce noise.
- Replaced the original BERT baseline with **RoBERTa + BPE tokenizer**, and converted SenticNet into **SPO triples** to prevent over-tokenization.
- Performed an ablation study to measure the impact of each noise-reduction component.

### Impact
- Accuracy improved from **64.4% (ConceptNet)** / **84.5% (naïve SenticNet)** → **88.1%**.  
- Removing key modules reduced performance (**–0.8 pp without soft-position**, **–2.7 pp without visible matrix**).

**In short:** I redesigned K-BERT’s knowledge integration to inject sentiment-specific information more intelligently, resulting in a cleaner and more accurate implicit-emotion classifier.
