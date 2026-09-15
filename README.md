# Total Frame

A free, browser-based picture framing calculator for framers, artists, collectors, and creative professionals. No install, no account — just open and start framing.

Use it at https://totalframe.pages.dev, or download `index.html` and open it in any browser. Everything runs client-side.

## Features

### Working Modes

- **Frame Priority** — Enter artwork/window and frame (rabbet) size; mat margins are calculated
- **Mat Priority** — Enter artwork size and the margins you want; frame size and moulding cut lengths are calculated

All results update as you type.

### Bottom Margin

- **Equal** — Uniform margins
- **Weighted** — Adds a fixed amount to the bottom (1/32″ steps)
- **Golden Ratio** — Bottom margin is 1.618× the top
- **Optical Center** — Artwork raised ~3% above geometric center

Golden and Optical show their offset — the equivalent bottom weight — in inches or mm.

### Window Offset

Reveal (opening larger than the art) or conceal (mat overlaps the art), linked or set per side. The mat size stays fixed and only the window edges move, in both modes. The previews show the backing board around the art on a reveal and the mat covering the art's edges on a conceal.

### Input

- Tap any dimension to open the numeric keypad: type whole numbers or decimals, add fractions with the slider (to 1/32″)
- Keypad: tall **CLR** key on the right, **Enter** at bottom right; Tab moves between Width and Height
- Arrow buttons step by 1/16″ (1/32″ for bottom weight) or 1 mm
- Imperial or metric

### Rabbet Depth Calculator

Stack-up of glazing, window mat (4-, 8- or 12-ply), optional spacer, back mat, backer and strainer, with a cross-section diagram.

### Frame Moulding Lengths

Cut lengths for each side (with ⅛″ fitting allowance) and minimum total moulding — Mat Priority.

### Visualizer

Close-up and Gallery Wall views, with optional artwork image upload (fill or ratio-lock).

### Batch Mode

Turn on **Batch** to save up to 200 jobs. Saved jobs go to the **Job List**.

### Job List

- One row per job: art/window, frame, sheet, orientation, mat colour
- Drag the handle on the left to reorder (numbers update); tick jobs to delete several at once, or Clear All
- **Load** a job back into the calculator (warns about unsaved changes)
- **Client / Project** name for the whole batch — shown on the exports and used for the file names
- **Export List** — one-page list PDF
- **Export List + Tear Sheets** — cover list plus one tear sheet per job

### CSV Import

**Import CSV** (next to Batch, or on the Job List) turns a spreadsheet into batch jobs. Choose a file or paste the rows, pick inches or millimetres, then review each row before adding.

```
Item,Window Width,Window Height,Frame Width,Frame Height,Orientation,Color,Mount Method,Window/Backer Only,Bottom Weight
SN00701488/104,7.375,9.75,14,17,V,Warm,Hinge,Y,0.125
SN00701488/127,4.75,6.6875,11,14,V,Warm,Hinge/Float,,
```

| Column | Meaning |
|---|---|
| Item | Job title / serial number |
| Window Width, Window Height | Window opening (decimals or fractions like `7 3/8`) |
| Frame Width, Frame Height | Frame (rabbet) size — **required**; each row is Frame Priority |
| Orientation | `V` or `H` — warns if the sizes disagree |
| Color | Mat board name, kept exactly as written and used to group the cutting plan |
| Mount Method | Label shown on the lists (e.g. Hinge, Corners) |
| Window/Backer Only | Blank = window + backer (2 boards). `Y` = one board: the window, or a backer if no window size is given |
| Bottom Weight | Blank = equal margins; a number = weighted bottom |

Only the frame size is required; blank optional columns aren't errors. Rows with problems are flagged in the preview and skipped. Imports are added to any jobs already in the batch.

### Mat Cutting Plan

Open from the Job List. Boards (windows and backers) are grouped by mat colour and nested onto stock sheets, cutlistoptimizer-style.

- **Per-colour cut list** — mat outer, window, top/bottom/left/right margins and bottom weight for each job (whole inches bold, decimal underneath)
- **Sheet diagrams** — every board labelled, window drop-outs dashed, reusable offcuts sized, cuts numbered in order; all cuts run edge to edge (straight-line cutter friendly)
- **Settings** (remembered):
  - Stock sheets: 32 × 40 only, 40 × 60 only, or both
  - Kerf (blade): default 1/32″
  - Edge trim: default none
  - Rotation allowed or off
  - Board size: Standard, or Full +1/16″ / +1/8″ per side for oversize boards
  - Knockouts: off, or reuse window knockouts (window minus 1/16″–1/4″ per side) to cut smaller boards — only used when it saves sheet board
- **Optimizer** — shows a quick layout instantly, then searches for about a second for fewer sheets / less board; the same batch always gives the same layout. Suggests a 1/16″ edge trim when that would save sheets
- **Download PDF** — vector PDF with the summary, cut lists, sheet diagrams and knockout diagrams

### Output

- **Mat Cut List** — Diagram with dimension lines, margin callouts and spec grid
- **Tear Sheet** — Job ticket with frame preview, spec table, item info and notes
- **PDF file names** use the Client / Project name with a `_tfcuts` suffix:

| Export | File |
|---|---|
| Export List + Tear Sheets | `client_project_tfcuts.pdf` |
| Export List | `client_project_tfcuts_list.pdf` |
| Mat Cutting Plan | `client_project_tfcuts_mat-plan.pdf` |

The job list, cover page and cutting plan are drawn as vector PDFs (sharp, small files). Tear sheets and the cut list are captured from the page. All PDFs use light-mode colours whatever the theme.

### Display

- Four themes: Light, Dark, Gray, Yellow
- Large-text mode for shop floor readability
- iPhone-friendly: keypad stays clear of the home bar

## Changelog

### v1.3

**New**

- **CSV Import** — Spreadsheet rows become batch jobs, with inches/mm choice and a per-row preview of errors and warnings
- **Mat Cutting Plan** — Boards grouped by mat colour and nested onto 32 × 40 / 40 × 60 sheets, with per-colour cut lists, numbered cut diagrams and a vector PDF
- **Knockout reuse** — Optionally cut smaller boards from window knockouts when it saves board
- **Full-size boards** — Account for oversize boards (+1/16″ or +1/8″ per side)
- **Job List** — Multi-select delete, Client / Project field, `_tfcuts` file names
- Batch limit raised from 30 to 200 jobs
- Golden / Optical bottom margin shows its offset; bottom weight steps in 1/32″

**Improved**

- Stronger sheet optimizer (look-ahead fill plus repacking), typically saving sheets on larger batches
- Export cover page redesigned as a vector job list; tear-sheet pages stored as JPEG (PDFs roughly 50–100× smaller)
- Mat Priority reveal/conceal now moves the window instead of enlarging the mat; previews show reveal and conceal correctly in both modes
- Keypad: CLR and Enter swapped (Enter bottom right), bottom row no longer hidden on iPhone
- Rabbet depth removed from the tear sheet
- Edge trim defaults to none

**Bug fixes**

- Fraction slider no longer jumps when you lift your finger
- Bottom Weight on the cut list and job list PDF reflected the real bottom margin mode

### v1.2

**New**

- **Batch Mode** — Save multiple jobs in a session with a floating Save button and running count
- **Job List** — Saved jobs in a table; drag to reorder; load any job back with unsaved-changes protection
- **Batch PDF Export** — List PDF, or list plus one tear sheet per item
- **Yellow theme**
- **Tab key** cycles Width ↔ Height while the keypad is open; Enter commits and closes
- **12-ply** window mat option in Rabbet Depth
- Auto-populated date in Item Info

**Improved**

- Mat Priority section order: Artwork → Mat Margins → Frame Size → Sheet Size → Window Offset → Bottom Margin
- Fractions under 1″ shown without a leading zero
- Bottom Weight and Sheet Size always shown on the cut list
- Project name sticky across batch saves; Item Info always open in Batch Mode
- All PDFs use light-mode colours

**Bug fixes**

- Metric keypad no longer shows the inch mark; subhint shows mm
- Unsaved-changes detection includes the artwork image
- Tab cycling works both ways for every Width ↔ Height pair

### v1.1

**Improved**

- Keypad display redesigned: whole number with stacked fraction, decimal below
- Sheet size shown in all three output views
- Balanced step buttons in Rabbet Depth

**Bug fixes**

- Tab commits the value and moves to the next field
- Fraction numerator no longer clips

## Tech

- React (Babel standalone — single HTML file, no build step)
- CSS custom properties for theming
- jsPDF for vector PDFs; html2canvas for captured pages
- Settings for the cutting plan stored in the browser (localStorage)
- PDFs use Helvetica — jsPDF only includes Helvetica, Times and Courier unless a font file is embedded

## License

Copyright © 2026 Christopher Cunningham. GNU General Public License v3.0.

## Acknowledgments

Written mostly with [Claude](https://claude.ai) by Anthropic.
