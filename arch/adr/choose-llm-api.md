# Choosing an LLM API

## Status

Initial ADR

## Context

LLMs will be used to serve the user with recipes that they request with the ability to discuss preferences, certain ingredients or replacements, and clarifying recipes.

## Decision

Model,Input (per 1M),Output (per 1M),Context Window
GPT-5.2 Pro,$21.00,$168.00,200K
GPT-5 (Standard),$10.00,$30.00,400K
Claude 4.6 Opus,$5.00,$25.00,1M
Gemini 3.1 Pro,$2.00,$12.00,2M

Model,Input (per 1M),Output (per 1M),Best For
Claude 4.6 Sonnet,$3.00,$15.00,Nuanced instruction following
GPT-5.4,$2.50,$10.00,Balanced reasoning/speed
GPT-5.2,$1.75,$14.00,High-speed performance
OpenAI o3,$2.00,$8.00,STEM & Logic reasoning

Model,Input (per 1M),Output (per 1M),Key Advantage
o4-mini,$1.10,$4.40,Strong reasoning for price
Claude 4.5 Haiku,$1.00,$5.00,"High speed, reliable JSON"
Gemini 3 Flash,$0.10,$0.40,Cheapest mainstream model
DeepSeek V3.2,$0.14,$0.28,Best raw value

From these three tables, Gemini appears to be the cheapest (outside of DeepSeek). I think the best choice would be a combination of Gemini 3 Flash and Gemini 3.1 Pro depending on the exact use case in the app. Recipe generation could be Gemini 3.1 Pro and Gemini 3 Flash could be used for quick questions regarding a recipe or ingredient.

Additionally, Gemini is currently my LLM of choice.

## Consequences

Create developer account for Google, perhaps if the Google Maps API is utilized there is a benefit to also using Gemini. Could also use image generation for recipes if user does not want to provide one