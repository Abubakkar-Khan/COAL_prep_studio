# COAL Exam Prep Studio

A single-page revision platform for **Computer Organization and Assembly Language (COAL / CS322)**. It turns local lecture notes, lab slides, scanned COAL pages, and past-paper photos into an interactive exam-preparation website.

**Live site:** [COAL Prep Studio](https://abubakkar-khan.github.io/COAL_prep_studio/)

The project is intentionally simple: open `index.html` in a browser and study. No build step, package manager, server, or internet connection is required.

## Features

- **Teacher Mode** with topic summaries, important facts, formulas, common traps, and exam-writing guidance.
- **Solved Exam Papers** grouped by visible past-paper photos, with compact model answers.
- **Mermaid-style rendered diagrams** generated offline from diagram definitions.
- **Interactive calculators and simulators** for common COAL exam tasks:
  - real-mode physical address calculation
  - FLAGS simulation
  - memory-bank visualization
  - descriptor/granularity decoding
  - endian storage
  - addressing modes
  - stack PUSH/POP
  - conditional jumps
- **Quiz Sprint** with a shuffled no-repeat deck, progress bar, answer reveal, scoring, and streak tracking.
- **Source Vault** for original scanned pages and past-paper images.
- **Last-night cheat sheets** for registers, FLAGS, addressing modes, instructions, protected mode, and formulas.

## Project Structure

```text
.
+-- index.html                  # Main COAL prep website
+-- preview.html                # Redirects to index.html for older browser tabs
+-- COAL.pdf                    # Original scanned COAL material
+-- Lect 05.pdf                 # Lecture 5 source material
+-- 8086 and 80386DX HW Specifications (24-25-26 Mar 2026).pdf
+                                # Scanned hardware pin/spec source
+-- COAL - Lab *.pptx           # Lab slide decks
+-- WhatsApp Image *.jpeg       # Original past-paper photos
+-- assets/
    +-- pages/                  # Extracted page images from COAL.pdf
    +-- past-papers/            # Normalized past-paper images
```

## How to Use

Open:

```text
index.html
```

in any modern browser.

If you still have `preview.html` open from an older version, refresh it. It redirects to `index.html`.

## Recommended Study Flow

1. Start with **Revision Roadmap** to choose a topic.
2. Open **Teacher Mode** and read the summary, important facts, formulas, and traps.
3. Use **Diagram Lab** to redraw the concept by hand.
4. Practice with **Exam Calculators**.
5. Review **Solved Exam Papers** for model answers.
6. Finish with **Quiz Sprint** and **Last-Night Cheat Sheets**.

## Key Topics Covered

- x86 and processor evolution
- CPU, memory, buses, and I/O basics
- number systems, signed values, storage units
- registers and FLAGS
- real-mode segment:offset addressing
- protected-mode selectors, GDT, LDT, descriptors, DPL/RPL
- memory banks and byte-enable signals
- 8086 and 80386DX hardware specifications, pins, logic levels, and bus-control signals
- assembly syntax and data definitions
- addressing modes
- data movement, endian storage, stack operations
- arithmetic, CMP, jumps, LOOP
- procedures, CALL/RET, DOS interrupts
- MASM assemble-link-run workflow

## Diagrams

The diagrams are rendered offline by JavaScript inside `index.html`. They are written as structured definitions and displayed in a Mermaid-like style, so the site works from a local `file://` URL without CDN access.

Current diagram categories:

- Memory
- Protected Mode
- Hardware
- Control Flow
- Assembly

## Notes for GitHub

This repository contains course PDFs, slide decks, and past-paper photos. Before making the repository public, confirm that you have permission to publish those files. If you only want to publish the website shell, remove or replace the source documents and generated source images first.

## Future Improvements

- Add a topic progress tracker with saved completion state in the browser.
- Add exam-mode practice sets: timed MCQs, short answers, and full past-paper attempts.
- Add searchable tags for every source page and past-paper image.
- Add printable one-page formula sheets for last-night revision.
- Add more worked examples for FLAGS, protected-mode descriptors, and memory-bank questions.
- Add a mistake notebook where students can save weak topics and revisit them before the exam.
- Add optional audio-style teacher notes or quick explainers for difficult topics.

## Development Notes

This is a static site. To edit it:

1. Modify `index.html`.
2. Refresh the browser.
3. Keep `preview.html` as a redirect unless you no longer need backward compatibility.

No dependencies are required for normal use.

## Verification Checklist

- `index.html` opens directly in a browser.
- `preview.html` redirects to `index.html`.
- Quiz Sprint advances to a new question.
- Physical address calculator returns `2FFF0h` for `CS=2F00h`, `IP=0FF0h`.
- Source Vault images load from `assets/pages` and `assets/past-papers`.
- Diagram Lab renders all diagram cards.

## License / Usage

No license has been selected yet. Add a `LICENSE` file before publishing publicly if you want others to reuse or modify the project.
