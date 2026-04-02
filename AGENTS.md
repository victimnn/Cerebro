#  Guidelines

## Project Structure & Module Organization
This repository is an Obsidian knowledge vault centered on economics notes. Core content lives under (./Economia), split by topic:

- `Economia/Autores/`: author profiles such as `Adam Smith.md`
- `Economia/Conceitos/`: concept notes such as `Livre mercado.md`
- `Economia/Correntes/`: schools of thought such as `Marginalismo.md`
- `Economia/Index.md`: entry point with links and study paths
- `Economia/Template *.md`: note templates for new content
- `.obsidian/`: local vault configuration; change only when intentionally updating workspace behavior

Keep new notes in the matching folder and preserve wiki-link relationships like `[[Livre mercado]]`.

## Build, Test, and Development Commands
There is no app build pipeline in this repository. Useful local commands are:

```powershell
git status
Get-ChildItem Economia -Recurse -Filter *.md
rg "\[\[.*\]\]" Economia
```

Use `git status` to review edits, `Get-ChildItem` to inspect note coverage, and `rg` to check internal links or naming consistency.

## Coding Style & Naming Conventions
Write in Markdown with short sections, direct explanations, and meaningful headings. Follow the existing templates:

- Start with a short definition or summary paragraph
- Use `##` section headings such as `Definição`, `Ideia central`, and `Importância`
- Prefer Portuguese note titles with spaces and accents when needed
- Use Obsidian wiki links instead of raw filenames where cross-referencing matters

Match the tone already used in (./Economia/Autores/Adam%20Smith.md): instructional, compact, and example-driven.

## Testing Guidelines
There is no automated test suite yet. Before opening a PR, verify:

- new notes follow the closest template
- all wiki links resolve to an existing note or an intentional placeholder
- `Economia/Index.md` is updated when adding major topics

## Commit & Pull Request Guidelines
Git history is currently sparse (`Initial commit`, `notas`, `a`), so adopt a clearer standard going forward. Use short imperative commit messages such as `Add Herbert Simon note` or `Update economia index links`.

PRs should include a brief summary, the folders changed, and screenshots only when `.obsidian/` layout changes affect navigation or presentation.
