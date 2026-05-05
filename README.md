# S-Parameter Viewer

A lightweight browser-based S-parameter viewer for RF engineering.

This tool reads Touchstone .s1p and .s2p files directly in the browser and plots magnitude response and Smith charts using Plotly.js.

## Live Demo

Add your Netlify link here:

https://your-site-name.netlify.app

## Features

- Supports .s1p and .s2p Touchstone files
- Drag-and-drop file upload
- Local file reading in the browser
- No server upload required
- Magnitude plot in dB
- Smith chart visualization
- S1P support:
  - S11 magnitude
  - S11 Smith chart
- S2P support:
  - S11, S21, S12, S22 magnitude
  - Selectable Smith chart for S11, S21, S12, and S22
- Frequency markers
- Default marker at 127.74 MHz
- Adjustable Y-axis range
- Frequency range slider
- Export plots as PNG images
- Dark UI designed for RF lab and engineering use

## Supported File Types

The viewer supports:

.s1p
.s2p

The file should follow the standard Touchstone format.

Supported data formats:

MA  Magnitude / Angle
DB  dB / Angle
RI  Real / Imaginary

Supported frequency units:

HZ
KHZ
MHZ
GHZ

## How to Use

1. Open the webpage.
2. Choose either S1P or S2P.
3. Drag and drop your Touchstone file into the upload area, or click to browse.
4. The viewer will automatically parse the file and display the plots.
5. Use markers to inspect specific frequencies.
6. Adjust the Y-axis range if needed.
7. Use the frequency range slider to zoom into a region.
8. Click Save PNG to export a plot.

## Privacy

Files are processed locally in the browser.

The uploaded .s1p or .s2p file is not sent to a server. The browser reads the file using JavaScript and plots the data on the client side.

This makes the tool suitable for quick lab analysis, sharing, and demonstration without uploading measurement data to external storage.


## Project Structure

For a simple deployment, the project can be as minimal as:

s-parameter-viewer/
  index.html
  README.md

The current implementation is contained in a single HTML file, including the HTML structure, CSS styling, and JavaScript logic.

## Dependencies

The viewer uses Plotly.js through a CDN:

<script src="https://cdn.plot.ly/plotly-2.27.0.min.js"></script>

No build system is required.

## Notes

- This viewer is intended for quick visualization and inspection of S-parameter data.
- It is not a replacement for full RF simulation, VNA software, or professional microwave design tools.
- Large Touchstone files may take longer to parse depending on the user's browser and computer performance.
- The Smith chart is generated in the browser and includes standard resistance and reactance grid lines.
