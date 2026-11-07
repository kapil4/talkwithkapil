# Instructions for Claude: the Talk with Kapil website

This repository is the live website **www.talkwithkapil.com**, served by GitHub Pages from `main`. Kapil isn't technical: Claude makes the changes, shows him a preview, and publishes only after he says yes.

## Workflow
1. Change words, prices, links and FAQs in `tools/build.py` only. `index.html` is generated, so never hand-edit it.
2. Run `python3 tools/build.py`. For style changes, edit `style.css`.
3. Preview before publishing. Serve the folder with `python3 -m http.server`, take Playwright screenshots at iPhone 13 size (full page; set `img[loading=lazy]` to eager first), and send them to Kapil.
4. After his OK, commit (with the session's attribution lines) and push to `main`. Then check that the GitHub run "pages build and deployment" finished: `gh api repos/kapil4/talkwithkapil/actions/runs`.
5. Check the live site in the built-in browser, in a fresh background tab. Never take over his tab-1.

## Hard rules
- Only true facts about Kapil: 10 years studying Vedic and Nadi jyotish, professional only since 2026, no psychology or counselling degree, no in-person sessions, no reviews yet. No made-up reviews, numbers or credentials.
- Never sell fear and never promise guaranteed results. Keep the disclaimer in the footer and the FAQ.
- Booking is WhatsApp first (`wa.me/919671115333` with a prefilled message ending "(website se)"), and UPI payment happens only after the time is fixed.
- Copy is written in Hinglish (Roman Hindi), matching his videos. Keep the brand palette (navy, gold, maroon) and the North Indian kundli motif.
- Don't touch GoDaddy DNS records other than `A @` and `CNAME www`, because the email records live there too.
- The rest of the brand rules are in the `talk-with-kapil-content` skill.
