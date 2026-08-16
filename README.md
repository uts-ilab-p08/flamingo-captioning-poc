# Flamingo - IDEFICS2 Captioning POC 

Evaluates whether IDEFICS2 (Image-aware Decoder Enhanced à la Flamingo with Interleaved Cross-attentionS, an open-access reproduction of Flamingo) can produce useful captions for MEVA surveillance frames — specifically, whether it describes actual activities rather than just generic scene content.

## Model choice: IDEFICS2

Using IDEFICS2 (Hugging Face) rather than the original DeepMind Flamingo, since Flamingo's weights were never publicly released. IDEFICS2 is a strong open vision-language model: SigLIP-SO400M vision encoder + Mistral-7B-v0.1, trained on OBELICS plus instruction-tuning on The Cauldron (50 curated
vision-language datasets), with native high-resolution input support (up to 980x980, aspect-ratio preserved) — relevant here given how small actors can be in a surveillance frame.
