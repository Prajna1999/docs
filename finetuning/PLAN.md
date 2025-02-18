Based on the repository and your background in backend development, here's what I recommend you do, in order:

1. **Start Small & Practical**
- Clone their repo and get their existing fine-tuning script working first (in `sft` directory)
- Use their most recent chat model: `TinyLlama-1.1B-Chat-v0.4` as your starting point
- Test with a small dataset before scaling up

2. **Your Environment**
- Single A100 or 2-3 RTX 4090s would be sufficient for fine-tuning
- Use their requirements.txt but add bitsandbytes for 4-bit quantization
- Don't try to replicate their full pretraining infrastructure

3. **Key Decision Points**
- What specific task are you trying to solve? This should drive your dataset choices
- How much compute do you actually have access to? This will determine quantization needs
- What's your inference environment? This affects your export format (GGUF vs native PyTorch)

Before you proceed, you should answer:
1. What's your specific use case/task?
2. What GPU resources do you have available?
3. How much data do you have for fine-tuning?

This will help determine the most efficient path forward rather than trying to tackle everything at once. Would you like to share these details so I can provide more targeted guidance?