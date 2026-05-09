# 🛡️ ContextGuard — AI Context Window Optimizer

> Stop wasting 40% of your LLM budget on bloated context windows.

ContextGuard automatically optimizes your AI context windows with three layers of intelligence: **deduplication**, **semantic compression**, and **smart truncation**. Save 30-50% on API costs without losing response quality.

## Why ContextGuard?

Every LLM request wastes tokens on:
- **Duplicated system prompts** (~25% waste) — same prompt sent every request
- **Bloated chat history** (~15% waste) — old irrelevant messages accumulate
- **Verbose tool schemas** (~10% waste) — unused function definitions eat tokens

**Result:** Teams spending $2,000/month on LLM APIs waste $600-$1,000 on tokens that add zero value.

## Features

- 🔍 **Deduplication Engine** — Hash-based + semantic duplicate detection
- 🗜️ **Semantic Compression** — Summarizes old turns, preserves key facts
- ✂️ **Smart Truncation** — Intelligent middle-cut, never breaks mid-sentence
- 🎯 **Tool Schema Filtering** — Only includes relevant tool definitions
- 📊 **Cost Analytics** — Real-time savings dashboard
- 🔌 **Framework Agnostic** — OpenAI, Anthropic, Google, Mistral, LangChain, LlamaIndex

## Quick Start

```bash
# Install
pip install contextguard

# Analyze a prompt file
contextguard analyze --file prompt.md

# Use as middleware
from contextguard import Optimizer
optimizer = Optimizer()
optimized = optimizer.optimize(messages=your_messages)
```

## API Usage

```bash
curl -X POST https://api.contextguard.io/v1/optimize \
  -H "Authorization: Bearer $CG_API_KEY" \
  -d '{"messages": [...], "model": "gpt-4o"}'
```

## Pricing

| Plan | Price | Features |
|------|-------|----------|
| Open Source | $0/forever | CLI, basic dedup, truncation, self-hosted |
| Pro | $29/mo | + Semantic compression, tool filtering, analytics, API |
| Team | $99/mo | + 25 seats, team analytics, SSO, priority support |

## Benchmarks

| Metric | Value |
|--------|-------|
| Average token reduction | 47% |
| Processing overhead | 0.3s per request |
| Accuracy preservation | 98.7% |
| Supported models | 15+ |

## Comparison

| Feature | ContextGuard | Manual | LangChain | LlamaIndex |
|---------|-------------|--------|-----------|------------|
| Auto deduplication | ✅ | ❌ | ❌ | ❌ |
| Semantic compression | ✅ | ❌ | ✅ | ✅ |
| Tool schema filtering | ✅ | ❌ | ❌ | ❌ |
| Framework agnostic | ✅ | ✅ | ❌ | ❌ |
| Cost analytics | ✅ | ❌ | ❌ | ❌ |

## License

MIT © 2026 ZOO Technologies
