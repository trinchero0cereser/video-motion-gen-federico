# video-motion-gen-federico

Kit unico per video e motion graphics con Claude Code. Fonde tre fonti:

| Fonte | Skill in `.claude/skills/` |
|---|---|
| **Remotion** (`remotion-dev/skills`) | `remotion-*` |
| **HyperFrames** (`heygen-com/hyperframes`) | `hyperframes*`, `remotion-to-hyperframes`, `figma`, `media-use`, `slideshow`, `style-sampling`, `reverse-any-video` |
| **Motion graphics per Opus** (`Barty-Bart/motion-graphics`) | `motion-broll`, `explainer-*`, `object-separation`, `sound-effects` |

Pacchetti npm: `remotion`, `@remotion/cli`, `react`, `react-dom`, `hyperframes`.

```bash
npm install
npx remotion studio
npx hyperframes --help
```
