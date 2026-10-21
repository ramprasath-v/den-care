# Amazon App Dev Hackathon 2026 submission checklist

The official rules remain authoritative: <https://amazonappdev2026.devpost.com/rules>. The submission deadline shown on the rules page is **October 23, 2026 at 12:00 PM Pacific Time**.

## Repository and access

- [ ] Commit and push the compliance files and final tested source to `https://github.com/ramprasath-v/den-care`.
- [ ] Confirm the repository remains public and GitHub detects the root MIT `LICENSE` in the repository header/About area.
- [ ] Put the repository URL in the Devpost submission.
- [ ] Confirm the public demo returns HTTP 200 with no login: <https://9umkurqacc.us-east-1.awsapprunner.com/>.
- [ ] Keep the repository, video, and a free judge-accessible project path available through the end of judging on November 20, 2026.
- [ ] Run the scoped synthetic-data reset before recording and before the judging window; do not expose AWS credentials or an unauthenticated reset endpoint.
- [ ] If the hosted demo becomes unavailable, keep the repository instructions and video sufficient for judging and restore the documented App Runner deployment promptly.

## Devpost fields

- [ ] Select **Alexa+** as the Primary Track.
- [ ] Select **AWS Builder** as the Mini Challenge.
- [ ] Describe Den as a **simulated Alexa+ experience**. Do not call it an official Alexa skill, official Alexa voice integration, or certified Alexa product.
- [ ] Explain the real MCP `2025-11-25` Streamable HTTP server as an additional implementation detail.
- [ ] Include a clear English description of features and functionality.
- [ ] Paste or adapt the factual feedback from `docs/product-feedback.md` for every tool/API/SDK used.
- [ ] Submit the strongest factual entries from `docs/friction-log.md` if claiming the optional friction-log bonus.
- [ ] List every contributor and confirm the entrant or team owns or is authorized to submit all project-authored work.
- [ ] If the project predates August 31, 2026, explain and demonstrate the significant updates made during the submission period. Current Git history shows project commits beginning September 27, 2026.

## Demonstration video

- [ ] Keep the video under three minutes; assume judges will not watch beyond three minutes.
- [ ] Show the project visibly functioning in its intended browser-based simulated Alexa+ experience.
- [ ] Show the public HTTPS URL, voice or typed request, real progress panel, approval gate, and persisted result.
- [ ] Upload the video publicly to YouTube or Vimeo and add its URL to Devpost.
- [ ] Use only project-owned or authorized footage, graphics, trademarks, music, and other material. The safest option is no background music.
- [ ] Keep all narration, captions, and testing instructions in English, or provide complete English translations.

## Final verification

- [ ] Run `PYTHONPATH=src .venv/bin/python -m pytest -q`.
- [ ] Run `node --check src/carecircle/web_assets/app.js` and `node tests/ui_state_refresh.cjs`.
- [ ] Run the exact demo only when safe, then restore the synthetic state with `scripts/reset_voice_demo.py --apply`.
- [ ] Scan tracked files and Git history for credentials, tokens, private keys, and local `.env` values.
- [ ] Confirm `.env`, `.venv`, caches, local AgentCore targets, SSO data, and generated build output remain untracked.
- [ ] Confirm the live description still states: synthetic data, simulated Ring provider, no diagnosis or dosing advice, no silent emergency calling, and no purchase or booking execution.
