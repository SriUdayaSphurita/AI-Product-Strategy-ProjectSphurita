# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | Heavy reliance on Stripe ACP model (and single LLM) | H | Introduce multi-provider routing layer (OpenAI + Anthropic fallback), abstract model calls behind a unified “Agent API Gateway” ie ACP Stripe|   
| **Abstraction** | Business logic partially coupled to vendor-specific tool calls / SDKs (model-dependent workflows) | H  |Build strict abstraction layer: intent → action → payment independent of model vendor; remove direct SDK dependency from core flow |
| **Routing** | Payment and decision routing logic partially embedded in AI workflow rather than external orchestration | M | Move routing logic out of AI: centralise in orchestration service (rules engine decides PSP routing, fraud checks, fallback paths) |
| **Eval** | Limited cross-model evaluation; performance metrics tied to one AI provider’s outputs | M | Implement continuous multi-model eval harness (OpenAI vs Anthropic vs others) with metrics: conversion rate, payment success rate, latency, fraud rate |

## Portability Score
<!-- Ready / Partial / Locked -->

## If [primary vendor] doubles pricing tomorrow:
<!-- What's your 48-hour response? -->

## If [primary vendor] ships a competing product:
<!-- What's defensible that they can't replicate? -->
