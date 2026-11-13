# DevSecOps, AEO (`llms.txt`) & Telegram + Kaspi FinTech (MurdaSoft Blocks 06, 07, 08)

## 1. Security & AEO (`llms.txt`)
- Bind Docker DB/Redis ports strictly to `127.0.0.1:5432:5432` to prevent UFW iptables bypass.
- Block SSRF on outbound user-supplied URLs (`127.0.0.1`, `169.254.169.254`, `10.0.0.0/8`, `192.168.0.0/16`).
- Serve `/llms.txt` at the domain root with clean Markdown summarizing product capabilities, API endpoints, and canonical links for AI Search engines (Perplexity, OpenAI Search, Google AI).

## 2. Telegram Mini Apps (TMA) + Kaspi QR / Pay
- Verify `Telegram.WebApp.initData` HMAC-SHA256 signature on the server before issuing a session.
- Use an explicit `idempotencyKey` (`UUID`) on payment creation and webhook handlers so duplicate callbacks never double-credit orders.
- Decouple Kaspi QR / Pay status polling + webhook reconciliation behind a dedicated payment adapter interface.
