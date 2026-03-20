# AGENTS.md

## Project
Build an agent that monitors a portfolio committee source link daily, detects new or materially changed content, analyzes what was newly communicated, and writes a report.

## Rules
- Always save the raw source before summarizing.
- Always compare current content to the previous saved version.
- Treat formatting-only changes as non-material.
- Output both Markdown and JSON.
- Never invent facts not found in the source.
- Log parsing failures clearly.
- Prefer small, testable Python modules.
- Add or update tests when changing parsing, diffing, or analysis logic.

## Output requirements
Each run must produce:
- raw source snapshot
- cleaned text
- change status: new / updated / unchanged
- summary of newly communicated items
- structured JSON with commitments, deadlines, entities, and issues

## Coding preferences
- Python 3.11
- Clear functions
- Minimal dependencies
- Use pathlib for file paths
- Use pytest for tests

## Report rules
The report must answer:
1. What is new?
2. Who communicated it?
3. What commitments or actions were mentioned?
4. What deadlines or follow-ups appear?
5. Why does it matter?
6. The officials involved or associated?
