<!-- managed by Lab - edit via Agents in the sidebar; changes here are overwritten on the next sync -->

<!-- agent: Code quality minimums -->
## Code quality minimums

These apply to every line of code in every repo. They override convenience.

### Fail fast, don't fail silent

If something fails, let it throw. No swallowed exceptions. No silent
fallbacks that mask the underlying problem. No retry loops that paper
over a broken contract. The error message is the diagnostic; if you
catch and rewrite it, you've thrown the diagnostic away.

The narrow exception: validate at system boundaries (user input,
external APIs, file system). Everything inside the boundary trusts the
contract.

### No fallbacks for impossible cases

Don't add error handling, validation, or fallbacks for scenarios that
can't happen. Trust internal code and framework guarantees. A `Result`
that's always `Ok` doesn't need to be a `Result`. A null check on a
value that's constructed three lines earlier is noise.

### No over-engineering

Don't add features, refactor, or introduce abstractions beyond what the
task requires. A bug fix doesn't need surrounding cleanup. A one-shot
operation doesn't need a helper function. Don't design for hypothetical
future requirements. Three similar lines is better than a premature
abstraction.

No half-finished implementations either. If you can't complete it, say
so and stop, don't leave a stub that compiles but lies.

### No decorative comments

Default to writing zero comments. Only add a comment when the WHY is
non-obvious: a hidden constraint, a subtle invariant, a workaround for
a specific bug, behavior that would surprise a reader. If removing the
comment wouldn't confuse a future reader, don't write it.

Don't explain WHAT the code does (well-named identifiers do that).
Don't reference the current task, fix, or callers ("used by X", "added
for the Y flow", "fixes #123"). Those belong in the PR description and
rot as the codebase evolves.

### No backwards-compat hacks for unused code

If something is unused, delete it completely. Don't rename to `_unused`,
don't add `// removed` comments, don't re-export removed types as
aliases. Backwards compatibility is for shipped public APIs (see the
Libraries category rule); internal scaffolding gets cut clean.


<!-- agent: Pixi rules -->
In pixi files:

The `project` field is deprecated. Use `workspace` instead.


<!-- agent: Static site conventions -->
## Static site conventions

For any site in this category. Currently small in scope; future-proofed
in case we add more.

### Static-only by default, no build step

If the site can ship as plain HTML/CSS/JS, it does. No Vite, no Next,
no Tailwind preprocess, no npm dependency tree. The reason is
operational: a marketing site that breaks because a transitive npm dep
got yanked is an embarrassing outage. A folder of static files cannot
break that way.

If a build step is genuinely required (e.g. blog with hundreds of
posts), the build output is what gets committed and served, not the
source. GitHub Pages serves what's in the branch.

### CNAME and .nojekyll are deployment infrastructure

`CNAME` pins the custom domain - don't delete it. `.nojekyll` disables
GitHub Pages' Jekyll preprocessing - don't delete it (it makes
underscore-prefixed paths work). If you do add a build step, replace
`.nojekyll` with the build output rather than re-enabling Jekyll.

### Mobile-first layout

Test in a phone viewport before merging. Hero animations especially:
big-screen-only effects that look great on a 27" monitor often stutter
or break the layout on a mid-tier phone. Image budget per asset: aim
for under 300KB, hard cap at 1MB. Use `loading="lazy"` for anything
below the fold.

### Marketing copy is SEO

The `<title>`, `<meta name="description">`, OpenGraph, and Twitter card
tags drive search snippets and link previews. Don't churn them
incidentally. Any change is effectively a marketing change and should
match the current product description (App Store metadata, TestFlight
description, README hero).

### External links rot

Beta invite URLs (TestFlight, Play Console internal testing) can be
revoked or rolled. Download links to GitHub Releases break when the
release is yanked. After any change to where these point, click the
live link in production. The site has no automated link-check; the
human eye is the only check.

### Hosted artifacts go in the repo, not in CI

If the site links to a binary download (alt-store IPA, sideload APK,
DMG), the binary lives in `downloads/` in the repo. Don't auto-populate
from CI - the moment CI starts pushing artifacts to a Pages-hosted
folder, you've turned a static site into a deploy target with secrets
and surface area.
