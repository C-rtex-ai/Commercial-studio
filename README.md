# Commercial Studio

**A production environment for creating videos with code and AI.**

Commercial Studio is an open-source project maintained by [C-rtex-AI](https://github.com/C-rtex-AI).

It brings together video production tools, motion design workflows and AI coding agents in one workspace. The goal is to make it possible to create commercials, product demos, motion graphics and other video content directly through code.

Instead of depending on expensive video platforms or manually editing every scene, the workflow allows AI agents to participate in the entire production process: from developing an idea and writing a script to building animations, working with audio and rendering the final video.

The ambition is simple: make code-driven video production more accessible, flexible and capable of producing genuinely good work.

## Why this project exists

Video production often involves a fragmented collection of tools. One application handles animation, another handles audio, and several paid services may be needed to complete a single project.

Commercial Studio takes a different approach.

It provides a reusable environment where creative direction and technical production can happen together. AI agents become part of the workflow, helping with both creative decisions and implementation.

This isn't about generating slides and calling them commercials. It's about building videos with intentional composition, meaningful motion, good storytelling and carefully designed sound.

## The toolkit

The environment combines several specialized tools.

| Tool | Purpose |
|---|---|
| **Remotion** | Main video engine. Videos are built with React and TypeScript. |
| **Extreme Motion Design** | Motion design workflow and production foundation. |
| **Motion Design Skill** | Principles for timing, easing, composition and animation. |
| **Motion Video Kit** | Creative direction, storytelling, storyboards and review. |
| **Barty Motion Graphics** | Sound effects workflow and audio analysis. |
| **Motion Starter Kit** | Visual references, styles and reusable ideas. |
| **Remotion Skills** | Official guidance for building videos with Remotion. |
| **FFmpeg** | Video and audio processing. |
| **Kokoro** | Local text-to-speech generation. |
| **Edge TTS** | An alternative voice generation option. |

Remotion is the primary renderer. Other tools are used when they provide a concrete benefit to the production workflow.

The toolkit is designed around free and locally available software wherever possible.

## Project structure

The workspace keeps shared resources, agent instructions and individual productions organized.

```text
Commercial-Studio/
│
├── .agents/
│   └── skills/             # Skills available to coding agents
│
├── .claude/
│   └── skills/             # Skills available to Claude Code
│
├── skills/
│   ├── extreme-motion-design/
│   ├── lottie-motion-design/
│   ├── motion-video-kit/
│   ├── barty-motion-graphics/
│   ├── motion-starter-kit/
│   └── remotion-skills/
│
├── projects/
│   ├── _template/          # Base template for new productions
│   └── my-commercial/      # Individual video projects
│
├── assets/                 # Shared images, audio and resources
├── references/             # Visual references and inspiration
├── output/                 # Final rendered videos
│
├── AGENTS.md
└── CLAUDE.md
```

Each production has its own directory, dependencies and assets. This keeps projects independent and makes it easier to experiment without affecting other productions.

## Getting started

### Requirements

The development environment uses Windows, but most of the tools are cross-platform.

You'll need:

- [Node.js](https://nodejs.org/)
- [Git](https://git-scm.com/)
- [FFmpeg](https://ffmpeg.org/)
- [Python](https://www.python.org/)
- [uv](https://docs.astral.sh/uv/)

### Setting up the workspace

Clone the repository and follow the setup instructions to install the required tools and skills.

Skills are organized locally in `skills/` and made available to compatible coding agents through `.agents/skills/` and `.claude/skills/`.

### Creating a production

Start by copying the shared template:

```powershell
robocopy .\projects\_template .\projects\my-commercial /E /XD node_modules .git
```

Install the project dependencies:

```powershell
cd .\projects\my-commercial
npm install
```

Use the scripts defined in the project's `package.json` to launch the Remotion Studio and render the video.

Each production should have its own creative brief, assets, scenes and final output.

## Production workflow

Commercial Studio is designed around a workflow that gives the creative process as much attention as the implementation.

1. **Concept development:** Understand the product, audience, message and objective. Explore creative concepts before jumping into animation.
2. **Creative direction:** Define the visual language, script, pacing and storyboard.
3. **Implementation:** Build scenes, transitions, typography, motion and effects in Remotion.
4. **Sound design:** Add narration, music and sound effects, paying attention to timing and synchronization.
5. **Review:** Evaluate composition, pacing, readability, audio and technical quality.
6. **Rendering:** Produce the final video after the result has been reviewed.

AI agents can participate throughout this process. They aren't limited to writing code: they can help develop concepts, critique scenes, propose improvements and handle production tasks.

## Design principles

A few principles guide the project:

- **Story comes first.** A technically impressive animation is still a weak commercial if it has nothing to communicate.
- **Motion has a purpose.** Animation should guide attention, communicate information or create emotion.
- **No slides disguised as videos.** Static layouts with basic transitions aren't the standard we're aiming for.
- **Quality over complexity.** More effects and layers don't automatically produce better work.
- **Reproducibility matters.** Prefer workflows that can be reused, understood and maintained.
- **Respect licensing.** Music, sound effects, images, fonts and other assets must have licenses compatible with their intended use.

The project prioritizes free and locally available tools. Some services may require an internet connection, and their availability or terms may change.

## Roadmap and direction

Commercial Studio is an evolving project. Its workflow and toolkit will continue to improve as new techniques and tools become useful.

Current priorities include:

- Improving the visual quality of Remotion-based productions.
- Making the workflow accessible to different AI coding agents.
- Developing reusable templates and animation techniques.
- Keeping voice generation and audio production accessible.
- Reducing unnecessary dependencies and reliance on paid services.
- Making the production process easier to reproduce across projects.

The long-term direction is to make the workflow feel natural: develop an idea, shape its creative direction, build it, review it and render it.

## Contributing

Contributions, suggestions and workflow improvements are welcome.

Whether it's a better animation technique, a useful skill, a more reliable production workflow or a tool worth integrating, improvements should help make the environment more capable without making it unnecessarily complicated.

Please open an issue to discuss significant changes before submitting a pull request.

## Credits and licensing

Commercial Studio brings together independently maintained tools and projects. Each dependency, skill and asset remains subject to its own license and terms.

Please check the original repositories and license files before redistributing or using third-party materials in commercial productions.

---

**Maintained by [C-rtex-AI](https://github.com/C-rtex-AI).**

*Built around a simple idea: video production should be limited by creativity, not by the tools.*