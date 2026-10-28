# DeceptIQ
### See beyond the link. Understand the deception. Stop the attack.

DeceptIQ is an explainable digital deception defense web prototype built by **Team Threat Forge** for HACKINDIA AI & CYBERTECH HACKATHON 2026.

It helps users understand why a link may be suspicious rather than returning only a black-box Safe/Unsafe verdict.

## Prototype features

- URL-level structural analysis using deterministic rules and heuristics
- Indicative risk score with contributing signals
- Manipulation-factor analysis
- Evidence-oriented findings and recommended actions
- Possible attack-chain visualization
- Analysis history and security reports
- Privacy and capability-limit disclosures

## Risk scoring

The current prototype uses a deterministic scoring approach:

- **Technical score:** sum of triggered technical-indicator weights, capped at 70.
- **Manipulation score:** average of five factors—urgency, fear, authority, reward, and sensitive request—each represented on a 0–100 scale.
- **Final score:** `min(100, Technical Score + 0.3 × Manipulation Score)`.

This is an **indicative risk score**, not a probability of fraud. The current weights are a prototype ruleset and should be calibrated against a representative labeled dataset before production use.

## Current limitations

- The prototype does not perform unrestricted live webpage inspection.
- Arbitrary URLs are analyzed at the URL level; controlled demo scenarios may use predefined sample page signals.
- It does not claim live external threat-intelligence lookups or an integrated external LLM for core scoring.
- A high or low score is not a guarantee that a site is malicious or safe.

## Development

The web app uses React, TypeScript, Vite, and Tailwind CSS.

```bash
npm install
npm run dev
```

## Team

**Team Threat Forge**  
**Product:** DeceptIQ

Built for HACKINDIA AI & CYBERTECH HACKATHON 2026.
