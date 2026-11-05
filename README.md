# claude-awesome-video-creation

**An Agent Skill for Claude Code that makes follow-along tutorial and explainer videos from code**: script, voice, picture, music, captions, a lip-synced mascot presenter, and measured QA.

```bash
npx skills add HaochenSHI66/claude-awesome-video-creation
```

Then, in your project, just ask Claude Code:

> make a 2-minute tutorial video about <feature>. Use the claude-awesome-video-creation skill.

or call it directly with `/claude-awesome-video-creation`.

## What it gives you
- **A follow-along structure**: hook → what it is → problem → how it works → STEP 1/2/3 with every command on screen → the real run → make your own → share → cheat sheet → "just the basics" + contact → call to action.
- **Voice-driven timing**: a beat-locked `timeline.ts` whose cues come from spoken words (`vs('s05', 'loads')`). Re-record a line and its animation, captions and mascot lip-sync follow.
- **A tutorial look**: navy stage with aurora light, macOS-style glass terminals (Cobalt2 blue, zsh prompt, syntax colours), colour-coded steps and labels.
- **A mascot presenter**: an original character pipeline (Codex image edits → magenta key → 19 sprites) with viseme lip-sync, blinking, typing, wave/point/cheer in-betweens, hop moves and turns, composited opaque so it never flickers.
- **Renders that finish**: segmented rendering that sidesteps a headless-Chrome GPU deadlock in heavy scenes; the on-screen render time is the measured one.
- **QA gates**: frozen-frame scan (no "buffering" moments), contact sheets, frame count, −14 LUFS loudness.
- **Lessons from real feedback**: `references/lessons.md` lists every request from a long iteration session with a student audience and the rule it became.
- **A complete worked example**: `assets/examples/teach-it-once/` is the full source of "Teach It Once", a 1:54 course video about Claude Code Agent Skills made with this skill.

## Layout
```
skills/claude-awesome-video-creation/
  SKILL.md                 entry point (modes, structure, rules, gates)
  references/lessons.md    feedback → rules (read first)
  references/voiceover.md  script format, TTS drafts, voice-clone hand-off
  references/look-tutorial.md  palette, glass windows, syntax colours
  references/mascot.md     original mascot pipeline
  references/render-qa.md  segmented render, QA gates
  references/cinetic-core.md + others   inherited cinetic craft guide
  scripts/                 render_segments.sh, check_static.py, sheet.sh, key_magenta.py, + cinetic scripts
  assets/examples/teach-it-once/   full film source + mascot sprites
```

## Credits
Built on [cinetic](https://github.com/Leonxlnx/cinetic) by Leonxlnx (MIT): its craft guide, scripts and starters are included and credited. This skill adds the tutorial mode, voiceover pipeline, mascot presenter, render/QA recipe and the lessons file.

Author: SHI Haochen · questions welcome: 24130819d@connect.polyu.hk · MIT License
