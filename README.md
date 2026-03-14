# Total Frame

A free, browser-based picture framing calculator for framers, artists, collectors, and creative professionals. No install, no account — just open and start framing.

## Changelog

### v1.2

**New**

- **Batch Mode** — Enable from the Measuring Options bar to save multiple jobs in a single session. Floating Save button with green flash confirmation and running count badge. Maximum 30 jobs per batch
- **Job List** — New tab showing all saved jobs in a table with Art/Window, Frame, Sheet, Orientation, and Mat Color columns. Drag-to-reorder with automatic renumbering. Load any job back into the calculator with unsaved-changes protection
- **Batch PDF Export** — Export List produces a clean tabular PDF; Export List + Tear Sheets produces a full multi-page PDF with a cover list and one tear sheet per item
- **Yellow theme** — New color theme (#ffeb7e background, #274044 text, #5eebff accent)
- **Tab key** cycles between Width and Height infinitely while the keypad is open. Enter commits and closes
- **12-ply** added to Rabbet Depth window mat options
- Auto-populated date in Item Info
- Cut list table reorganized: left column shows Window Opening, Mat Outer, Sheet Size, Bottom Weight; right column always shows Top, Left, Right, Bottom margins
- PDF exports always render in light mode regardless of current theme

**Improved**

- Mat Priority section order: Artwork → Mat Margins → Frame Size → Sheet Size → Window Offset → Bottom Margin
- "Calculated Dimensions" renamed to "Frame Size" in Mat Priority — now shows outer frame dimensions
- Fraction values under 1″ no longer show leading zero (½″ instead of 0 ½″)
- Bottom Weight always shown on cut list (Equal/Golden/Optical/weighted amount)
- Sheet Size always shown on cut list ("Not specified" when off)
- Mat and frame color names shown bold uppercase on cut list and tear sheet headers
- Cut Here line removed from tear sheet; notes section expanded to 5 lines
- Item Info section always open when Batch Mode is active
- Project name sticky across batch saves
- All PDFs use light mode colors for consistent print output

**Bug fixes**

- Metric keypad no longer shows inch (″) mark
- Metric keypad subhint now shows mm value in accent color
- Unsaved changes detection now includes artwork image
- Tab cycling fixed — all Width↔Height pairs cycle two-way
- Section glitch on mode switch resolved using display:none instead of conditional rendering

### v1.1

**New**

- Sheet size now appears in all three output views
- Rabbet Depth section shows balanced step buttons on both sides of each row
- Section divider lines slightly heavier for better visual separation

**Improved**

- Keypad display redesigned: unified whole number + stacked fraction, decimal below
- Keypad key layout updated: CLR top-right, 0 under 1, Enter spans full right column
- Fraction digit sizes increased slightly
- Accent color updated to more vibrant mid-tone blue

**Bug fixes**

- Tab key now commits value and moves to next field
- Fraction numerator no longer clips in FractionPicker
- Label-to-value spacing corrected

## Features

### Working Modes

- **Frame Priority** — Enter frame (rabbet) size, get mat margins automatically
- **Mat Priority** — Enter artwork size and desired margins, get frame size and moulding cut lengths

### Margin Calculations

- **Equal** — Uniform margins on all sides
- **Weighted** — Adds a fixed amount to the bottom
- **Golden Ratio** — Bottom derived from golden ratio (×1.618)
- **Optical Center** — Shifts artwork ~3% above geometric center

### Window Offset

Reveal/conceal adjustments, linked or independent per side.

### Input

- Tap-to-open numeric keypad with fraction slider (1/32″ precision)
- Tab key cycles Width↔Height infinitely without closing the keyboard. Enter commits and closes
- Arrow buttons step by 1/16″ or 1mm
- Metric mode available

### Batch Mode

Save up to 30 jobs per session. Drag-to-reorder job list with automatic renumbering. Load any saved job back into the calculator. Export as a list PDF or full multi-page PDF with tear sheets.

### Rabbet Depth Calculator

Stack-up for glazing, window mat (4-ply, 8-ply, 12-ply), optional spacer, back mat, backer board, and strainer. Visual cross-section diagram to scale.

### Frame Moulding Cut Lengths

All four sides with ⅛″ kerf allowance.

### Visualizer

Close-up and Gallery Wall views. Optional artwork image upload with fill or ratio-lock modes.

### Color & Display

- Four themes: Light, Dark, Gray, Yellow
- Large-text mode for shop floor readability
- All PDFs render in light mode regardless of active theme

### Output

**Mat Cut List** — Diagram with dimension lines, margin callouts, and spec grid.

**Tear Sheet** — Job ticket with frame preview, spec table, Item Info, and five-line notes section.

**Job List PDF** — Tabular summary, or combined multi-page PDF with tear sheets.

## Usage

https://totalframe.pages.dev

Or download the single HTML file and open in any browser — fully client-side.

## Tech

- React (Babel standalone — single HTML file, no build step)
- Vanilla CSS custom properties for theming
- html2canvas + jsPDF for PDF export

## License

Copyright © 2026 Christopher Cunningham. GNU General Public License v3.0.

## Acknowledgments

Written mostly with [Claude](https://claude.ai) by Anthropic.
