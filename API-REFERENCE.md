# ShieldFlow AI - API Reference

This is a sample of what our API looks like. The full API is available when you deploy ShieldFlow.

## Base URL
https://api.shieldflow.ai/v1

text
or when self-hosted:
http://your-server:5190/api/v1

text

## Authentication
All requests require an API key:
```http
X-API-Key: your-api-key-here
Quick Examples
Scan Text
bash
curl -X POST https://api.shieldflow.ai/v1/scan/text \
  -H "X-API-Key: your-key" \
  -H "Content-Type: application/json" \
  -d '{"text":"Check this content for safety"}'
Batch Scan
bash
curl -X POST https://api.shieldflow.ai/v1/scan/batch \
  -H "X-API-Key: your-key" \
  -H "Content-Type: application/json" \
  -d '{"texts":["First piece","Second piece","Third piece"]}'
Common Responses
Safe Content
json
{
  "id": "scan_123",
  "text": "Hello, how are you?",
  "isSafe": true,
  "riskLevel": "NONE",
  "flags": [],
  "processingTimeMs": 4
}
Flagged Content
json
{
  "id": "scan_456",
  "text": "This contains an email: test@example.com",
  "isSafe": false,
  "riskLevel": "MEDIUM",
  "flags": ["PII_DETECTED"],
  "details": "Personal information found",
  "processingTimeMs": 7
}
Blocked Content
json
{
  "id": "scan_789",
  "text": "Inappropriate content here",
  "isSafe": false,
  "riskLevel": "CRITICAL",
  "flags": ["INAPPROPRIATE_CONTENT"],
  "action": "BLOCK",
  "details": "Content violates safety rules",
  "processingTimeMs": 5
}
Rate Limits
Free tier: 100 requests/hour

Standard: 1,000 requests/hour

Business: 10,000 requests/hour

Enterprise: Custom limits

Webhooks (Coming Soon)
Set up webhooks to get notified when:

Content is blocked

High-risk content detected

Daily usage reports

System alerts
