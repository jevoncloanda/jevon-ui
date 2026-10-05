# jevon-ui

A portable personal Codex skill for Jevon's UI preferences, project/domain fit, preservation of repository conventions, and visual-reference interpretation.

`jevon-ui` supplies personal design judgment and project fit. **Impeccable** supplies a complementary broad design toolkit: design theory, shaping, audit, critique, polish, anti-pattern analysis, and browser-oriented iteration. Impeccable is optional but recommended for substantial design work; install both skills independently. Nothing from Impeccable is vendored here, and Jevon UI still works when it is unavailable.

It is not a component library, build system, universal palette, or mandate to make every product minimal, dense, square, or look like Linear. Existing products should retain their identity; different products should look different.

## Contents

```text
jevon-ui/
├── .gitignore
├── SKILL.md
├── README.md
├── references/
│   ├── jevon-principles.md
│   ├── reference-workflow.md
│   ├── project-context.md
│   └── review-checklist.md
└── evals/
    └── cases.md
```

`SKILL.md` contains execution guidance. Supporting files are read only when relevant. No runtime dependencies are required.

## Installation

Keep this repository as the canonical copy, for example at `~/Code/jevon-ui`. Current [official Codex documentation](https://developers.openai.com/codex/skills) documents `~/.agents/skills` for user-wide skills and supports symlinked skill folders. This local installation also exposes skills in `~/.codex/skills`; prefer the documented `.agents` location for new portable installations. Install only one copy to avoid duplicate skill entries.

The commands below assume the clone is at `~/Code/jevon-ui`. Adjust the source if needed. They stop when the destination already exists; inspect the existing installation before replacing it.

### Windows (PowerShell)

Choose **one** installation method:

```powershell
$skillSource = Join-Path $HOME 'Code/jevon-ui'
$skillRoot = Join-Path $HOME '.agents/skills'
$skillTarget = Join-Path $skillRoot 'jevon-ui'
if (-not (Test-Path -LiteralPath (Join-Path $skillSource 'SKILL.md'))) {
    throw 'The source is not a jevon-ui skill clone.'
}
New-Item -ItemType Directory -Path $skillRoot -Force | Out-Null
if (Test-Path -LiteralPath $skillTarget) { throw 'jevon-ui is already installed.' }

# Preferred for development: link to the canonical clone.
New-Item -ItemType SymbolicLink -Path $skillTarget -Target $skillSource

# Alternative copy installation: run this instead of New-Item SymbolicLink.
# Copy-Item -LiteralPath $skillSource -Destination $skillTarget -Recurse
```

Windows symbolic links may require Developer Mode or an elevated PowerShell session, depending on system policy. A directory junction (`-ItemType Junction`) is an alternative for a local directory; copying avoids link permissions. Keep the clone at its linked location.

### macOS/Linux

Choose **one** installation method:

```sh
skill_source="$HOME/Code/jevon-ui"
skill_root="$HOME/.agents/skills"
skill_target="$skill_root/jevon-ui"
(
  set -eu
  test -f "$skill_source/SKILL.md" || { echo 'The source is not a jevon-ui skill clone.' >&2; exit 1; }
  mkdir -p "$skill_root"
  if [ -e "$skill_target" ] || [ -L "$skill_target" ]; then
    echo 'jevon-ui is already installed.' >&2
    exit 1
  fi

  # Preferred for development: link to the canonical clone.
  ln -s "$skill_source" "$skill_target"

  # Alternative copy installation: run this instead of ln.
  # cp -R "$skill_source" "$skill_target"
)
```

Copy installations may include the clone's Git metadata; transfer `SKILL.md`, `references/`, and `evals/` together, preserving relative paths. README is useful for maintenance but is not required for invocation.

## Use and discovery

Codex exposes the skill's name and description for selection, then loads the instructions when invoked. Automatic selection is enabled by default; there is no explicit-only policy. The description targets meaningful visual work, including dashboards, forms, data tables, responsive layouts, design review, and screenshot/Figma/live-site implementation. It excludes backend/database/infrastructure/API-only work, nonvisual frontend refactors, and tiny implementation changes without visual impact.

Tiny alignment or button-copy fixes use repository conventions without a full preflight or Impeccable workflow. For substantial new UI, Jevon UI establishes constraints and may use Impeccable shaping or general guidance. For an unfinished existing screen, polish, audit, or critique may help while preserving the product. Selecting an Impeccable workflow means reading and following its installed playbook; this repository does not duplicate its command catalog.

Explicit invocation:

```text
Use $jevon-ui to review a hypothetical operations dashboard.
```

Codex detects skill changes automatically according to the official documentation. If the skill does not appear, restart Codex and check its skill selector for `jevon-ui`. A session's already-loaded skill catalog may not refresh immediately. Successfully parsing metadata does not prove automatic selection for every future prompt.

## Project direction

Within design guidance, precedence is: explicit user requirements; project design specification; scoped user references; repository/product conventions; domain and workflow; Jevon UI preferences; Impeccable generic recommendations. System and repository instructions remain authoritative. Generic advice must not erase intentional product identity.

Classify each surface as product or brand/marketing before substantial work. Product interfaces favor efficient tasks, clear state, and appropriate density; brand, campaign, and portfolio surfaces allow more expression and storytelling. Scope each visual reference to the characteristics it should influence, then adapt and verify that scope rather than cloning unrelated branding or blindly blending sources.

Recommend `PRODUCT.md` for users, tasks, workflows, constraints, and information priorities, and `DESIGN.md` for visual identity, tokens, components, density, navigation, responsive rules, references, and intentional deviations when durable context helps. Preserve existing locations such as `docs/DESIGN.md`; neither file is mandatory or automatically created for small tasks. See [project context guidance](references/project-context.md).

Meaningful visual work includes inspecting the running interface at realistic widths and relevant states, fixing issues, and reinspecting. Build/lint/type checks alone do not establish visual quality. If browser verification is unavailable, the agent should identify the missing proof.

## Updates and other computers

On another computer, clone the repository or transfer its files, then repeat one installation method using that computer's home directory. No usernames, absolute machine paths, or local tooling dependencies are embedded in the skill.

Update the canonical clone using your normal Git workflow (for example `git pull --ff-only` after publishing and configuring a remote). Linked installations use changes immediately; for copies, first confirm the installed folder has no edits to preserve, then replace the copied skill resources with the updated versions. Do not blindly overwrite local changes.

Validate metadata with Codex's bundled `skill-creator/scripts/quick_validate.py` when available; this validator is development tooling, not a skill dependency. Also check relative links and review [behavioral eval cases](evals/cases.md), including trigger boundaries, preservation, explicit aesthetics, reference scopes, optional Impeccable use, and missing tooling. Packaging and conceptual checks cannot prove runtime design judgment or automatic triggering; test selection in a fresh session and verify actual rendered outcomes.
