# Total Frame

A free, browser-based picture framing calculator for framers, artists, collectors, and creative professionals. No install, no account — just open and start framing.
Use it now at https://totalframe.pages.dev

## Features

### Working Modes

Two calculation modes to match your workflow:

- **Frame Priority** — Enter frame (rabbet) size, get mat margins calculated automatically
- **Mat Priority** — Enter artwork size and desired mat margins, get the required frame size

All calculations update in real time as you type.

### Margin Calculations

Four margin modes for the bottom margin when using frame priority:

- **Equal** — Uniform margins on all sides
- **Weighted** — Adds a fixed amount to the bottom margin
- **Golden Ratio** — Bottom margin derived from the golden ratio
- **Optical Center** — Shifts artwork up for perceived visual centering

### Window Offset

Reveal and conceal adjustments to control how much artwork edge is visible or hidden under the mat. Offsets can be linked (uniform) or set independently per side.

### Input

- Tap-to-open numeric keypad with integrated fraction slider
- Increment/decrement arrow buttons for fine adjustments
- All dimensions display as fractional inches to 1/32″
- Metric conversion available

### Rabbet Depth Calculator

A stack-up calculator that accounts for glazing, window mat ply (4-ply / 8-ply), optional spacer, back mat, and backer board. Includes a visual cross-section diagram showing each layer and the total depth relative to the rabbet.

### Frame Moulding Cut Lengths

Automatically calculates moulding lengths for all four sides with a ⅛″ kerf allowance per cut.

### Visualizer

- **Close-up** — Detailed view of the framed piece with accurate mat and frame colors
- **Gallery Wall** — Shows the piece hung at standard height with a human figure for scale
- Optional artwork image upload with fill or aspect-ratio fit modes
- Responsive scaling for mobile and desktop

### Color & Display

- Three color themes (light, dark, gray)
- Large-text mode for shop floor readability

### Output

**Mat Cut List** — An engineering-style diagram with full dimension lines, margin callouts, and a two-column specification grid. Shows all measurements needed to cut the mat.

**Tear Sheet** — A project specification job ticket with a mini frame preview, complete spec table, optional write-in fields for project/client info, and a notes section.

Both pages are printable and exportable as PDF.

## Usage

Use it now at https://totalframe.pages.dev

Or download the HTML file and open it in any browser — everything runs client-side, no server required.

## Tech

- React (Babel standalone — single HTML file, no build step)
- Vanilla CSS custom properties for theming
- jsPDF for PDF export

## License

Copyright © 2026 Christopher Cunningham

This project is licensed under the GNU General Public License v3.0. See [LICENSE](LICENSE) for details.

## Acknowledgments

Written mostly with [Claude](https://claude.ai) by Anthropic.
