# MENA Creator Workflow

A portable, evidence-aware workflow for creator marketing across MENA markets. It helps brand teams, agencies, and advisors turn campaign briefs into clearer creator scripts, review notes, and concise briefs.

## The problem it addresses

Creator work crosses people with different responsibilities: brand owners set goals and guardrails, agencies prepare and review deliverables, advisors shape positioning and tests, and creators bring their own voice and production constraints. A sector-only checklist can miss who owns a decision; a role-only checklist can miss what a credible story looks like for the product.

This skill makes those two axes explicit. It ties script feedback to brief requirements, observable evidence, specific lines or shots, and the person who owns an open decision. It helps teams revise work while preserving creator intent where the brief allows.

## Role × industry routing

The role and client-industry axes are read separately. The user's goal and current brief take precedence over defaults.

| Collaboration role | Emphasis |
|---|---|
| Brand / growth team | Objective, audience, constraints, brand guardrails, evidence, and acceptance criteria |
| Agency execution partner | Feasibility, deliverable readiness, creator coordination within established authorization, revision tracking, and approval trail |
| Consultant / advisor | Positioning, route to market, channel choice, and experiments with a learning question and success signal |

| Client industry | Useful default lens |
|---|---|
| E-commerce / consumer goods | Creator breadth, visible use, conversion-aligned CTA, when supported by the brief |
| Consumer electronics / hard tech | Observable practical value and substantiated product claims |
| AI products | A relevant trend and supported workflow change, without unsupported breakthrough claims |

These are starting points, not sector rules. The complete routing notes are in [`references/role-industry.md`](references/role-industry.md).

## Main outputs

- **Script review and revision:** map brief requirements to shots, lines, proof, timing, CTA, and open decisions; provide specific supported edits.
- **Short creator brief:** give a creator the goal, core message, proof, required or avoided content, CTA, timing, and approval path in a compact format.
- **Light GTM and experiment note:** outline a positioning hypothesis, route to market, channel test, learning question, and decision needed. This is a lightweight structure, not specialist GTM consulting.

The script workflow can return both a revised storyboard and a requirement-coverage table. For Saudi Arabic, it adds a market-specific voice review aid; it does not claim native-speaker quality. Other MENA markets should use their requested dialect or register.

## Quick start

Choose the mode your host supports. The core is plain Markdown with YAML frontmatter and relative links to its supporting files.

### 1. Native Skill host

Import the `mena-creator-workflow/` folder using the host's Skills interface and invoke it by its registered name. In Codex, place the folder under `~/.codex/skills/mena-creator-workflow/` and invoke `$mena-creator-workflow` when it is available. Manus documents uploading a local ZIP, `.skill` file, or folder in its Skills interface; this repository itself contains the skill folder and may be uploaded as an archive. See [Manus Skills documentation](https://manus.im/docs/features/skills).

### 2. File-based project

Add the folder to the project (or the host's recognized skill directory). In project instructions, tell the assistant to read `SKILL.md` for creator-workflow tasks and load only the relevant linked files under `references/`, `assets/`, or `examples/`. Follow that host's directory convention; a generic `skills/` folder is not guaranteed to auto-load.

### 3. Prompt-only host

Paste the contents of `SKILL.md` into the instruction context and attach the supporting files needed for the current task. Explicitly ask the assistant to use those attachments. Do not assume that an assistant can read relative links from pasted text or discover the other files automatically.

## Anonymized before / after example

These synthetic examples use placeholders only; they are not real client approvals or product tests.

**Before:** A 40-second script header sits above timed sections totaling 50 seconds. The creator says “Phone A is better in low light,” while speaking to a front-facing camera in the opening. A later rear-camera comparison with Phone B is planned but has not been filmed; the creator does not want to feature a competitor.

**After review:** Keep the selfie-camera opening if it is only creator B-roll; it is not itself a comparison sample. Flag the runtime mismatch and mark the performance claim unproven until usable comparison footage is reviewed under fair conditions. Mark competitor appearance as a pending client–creator decision, with options such as a standalone Phone A demo, rights-cleared supplied footage, or a comparison only if the creator agrees. Do not label any option approved or invent an offer for the CTA.

A fuller synthetic example is in [`examples/anonymized-camera-review.md`](examples/anonymized-camera-review.md).

### Arabic copy review

**Before:** `تقدم هذه الكاميرا أداءً استثنائيًا في جميع الظروف.`

**Proposed rewrite:** `خلّنا نجربها هنا ونشوف كيف تطلع الصورة.`

This is not an equivalent translation. The original promises exceptional performance in every condition without supplied evidence. The rewrite invites a test in the scene at hand; it does not claim a result. Use it only if the creator will actually film that test, then review the footage before making a performance claim. Here, language editing and fact review work together.

## Project status

Version 1 is a compact first draft. Structure was checked with the Skill Creator validator, and relative links were checked separately. Cross-platform behavioral validation is pending; no benchmark has been run.

The workflow does not certify product facts, approve scripts on behalf of a brand or creator, or authorize external messages or publishing. Saudi Arabic guidance is an editing aid, not a guarantee of native speech.

## Repository map

```text
mena-creator-workflow/
├── SKILL.md
├── references/
│   ├── role-industry.md
│   ├── script-review.md
│   └── saudi-arabic-review.md
├── assets/
│   └── output-templates.md
└── examples/
    └── anonymized-camera-review.md
```

## Author and attribution

Domain design and editorial review by Aaron Hu; developed with AI coding assistance. Contributions include creator-workflow framing, role and industry routing, script review, output templates, and synthetic examples. GitHub account: [hcj00112233](https://github.com/hcj00112233).

The Saudi Arabic review aid adapts principles from the user-provided `saudi-native-arabic` skill. It has been condensed and reframed for creator-script review; the original skill is not included in this repository.

## License

The standard MIT license in [`LICENSE`](LICENSE) applies to the original materials authored for this repository. The referenced `saudi-native-arabic` skill is not included here and retains its own authorship and terms.
