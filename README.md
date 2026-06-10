# throughline-media

Static media for [Throughline Studio](https://throughline-studio.vercel.app) —
the narrated walkthrough videos for the 20 worked examples (`videos/<slug>.mp4`),
served via GitHub Pages so the app repo stays lean.

Each video is rendered from the Remotion project at `E:\video\throughline-explainer`
(`CaseStudy` composition + `props/<slug>.json`); narration is generated with
edge-tts from the hand-verified case-study fields in
`throughline-studio/src/lib/caseStudies.ts`. Every paper fact is DOI-verified;
the seven-stage journey is explicitly framed as a reconstruction.

Regenerate: `python gen-case-narration.py` then `render-cases.ps1` in the
Remotion project, copy `out/cases/*.mp4` here, commit, push.
