
# ShieldFlow AI - Content Safety Platform

This is the public documentation for ShieldFlow AI. If you're looking for the source code, it's in a private repository - ShieldFlow is a commercial product we're building and selling.

## What We're Building

We're making a content safety API that does what Azure Content Safety does, but cheaper and with more control. Right now we have a solid rules-based system that catches inappropriate content, personal information, and prompt injection attempts. We're working on adding Microsoft's DeBERTa model to make it even smarter.

## The Problem We're Solving

Azure charges $1.50 for every 1,000 pieces of content you scan. If you have user-generated content at any scale, that adds up fast. We're building something that gives you the same kind of safety checks, but you run it on your own servers and pay a fraction of the cost.

## How It Compares

| | Using Azure | Using ShieldFlow |
|---|---|---|
| **Cost** | $1.50 per 1,000 calls | $0.15 per 1,000 calls |
| **Where it runs** | Microsoft's servers | Your servers |
| **Your data** | Goes to Microsoft | Stays with you |
| **Speed** | 50-200ms (network time) | <10ms (local) |
| **Can you customize it?** | Not really | Yes, completely |

## What Works Today

The current version catches:
- Inappropriate content (with rules and patterns)
- Personal information like emails and phone numbers
- Prompt injection attempts
- Basic toxicity and hate speech

## What We're Adding

We're integrating Microsoft's DeBERTa model (the same technology Azure uses) to catch more subtle issues:
- Nuanced toxicity
- Context-dependent inappropriate content
- Better hate speech detection
- Smarter pattern recognition

## For Developers

If you're technical and want to know what's under the hood:
- Built with .NET 9.0
- Docker and Kubernetes ready
- REST API with Swagger docs
- API key authentication
- Multi-tenant support

## Getting Access

Since this is a product we're selling:
1. Contact us for a demo
2. We can set up a trial
3. You can run it on your servers or use our hosted version
4. Pricing starts at $0.15 per 1,000 requests (much cheaper than Azure's $1.50)

## Contact

Want to try it or have questions?
- Email: contact@shieldflow.ai
- Demo requests: demo@shieldflow.ai
- Technical questions: tech@shieldflow.ai

---

*Just to be clear: This repo has documentation and information. The actual code is in a private repository because ShieldFlow is a commercial product we're actively developing and selling.*

*Last updated by Imed Tag: 31 December 2025*
 
