# FlowChart

A lightweight repository for documenting and maintaining business process flowcharts using **draw.io** and web-based previews.

## Overview

This repository stores editable process diagrams together with documentation and browser-friendly previews.

The main diagram currently documented in this repository is **LCV FlowChart**, covering the flow between:

- Power Apps
- SharePoint Online
- Power Automate
- UiPath
- UiPath Queue
- SharePoint On-Premises
- Excel generation

## LCV FlowChart

### Process Overview

The LCV process starts when a user submits data through Power Apps. The data is stored in SharePoint Online and then processed by Power Automate.

The process includes program-type decisions that determine the subsequent Power Automate and UiPath actions.

High-level flow:

```text
Power Apps
    │
    ▼
SharePoint Online
    │
    ▼
Power Automate
    │
    ▼
Program Budaya?
    ├── Bestie
    │     └── Rename / Queue processing
    │
    └── Selain Bestie
          └── Queue processing
                    │
                    ▼
                  UiPath
                    │
                    ▼
              Program Budaya?
               ├── Bestie
               │     ├── Download document
               │     └── Upload to SharePoint On-Premises
               │
               └── Selain Bestie
                     └── Create Excel
                           │
                           ▼
                Upload to SharePoint On-Premises
```

### Preview

**[Open LCV FlowChart in diagrams.net](https://viewer.diagrams.net/?url=https%3A%2F%2Fraw.githubusercontent.com%2Ffajarinsanfi-ops%2FFlowChart%2Fmain%2FLCV_FlowChart)**

The preview opens the original diagram directly in the diagrams.net viewer.

### Source File

[**LCV_FlowChart**](./LCV_FlowChart)

The source file is maintained in the repository as the editable master diagram.

## Process Components

| Component | Role |
|---|---|
| Power Apps | User interface for submitting LCV data |
| SharePoint Online | Stores submitted data |
| Power Automate | Retrieves and processes the latest data |
| UiPath Queue | Receives queue information for automation |
| UiPath | Processes LCV documents and generates output |
| SharePoint On-Premises | Final destination for processed documents and generated files |
| Excel | Output generated for applicable program types |

## Repository Structure

```text
FlowChart/
├── README.md
├── index.html
├── style.css
├── flowchart.md
└── LCV_FlowChart
```

### File Description

| File | Description |
|---|---|
| `README.md` | Project and process documentation |
| `index.html` | Browser-based flowchart page |
| `style.css` | Styling for the browser page |
| `flowchart.md` | Mermaid flowchart source/example |
| `LCV_FlowChart` | Editable draw.io XML diagram |

## Working With LCV_FlowChart

### Open the editable diagram

Use **draw.io / diagrams.net** and open:

```text
LCV_FlowChart
```

You can use the online editor at:

**[diagrams.net](https://app.diagrams.net/)**

### View without editing

Use the README preview:

**[Open LCV FlowChart Preview](https://viewer.diagrams.net/?url=https%3A%2F%2Fraw.githubusercontent.com%2Ffajarinsanfi-ops%2FFlowChart%2Fmain%2FLCV_FlowChart)**

### Update the diagram

1. Open `LCV_FlowChart` in diagrams.net.
2. Make the required process or layout changes.
3. Save/export the updated diagram.
4. Replace the repository source file.
5. Update this README if the process logic has changed.

## Browser Flowchart

The repository also contains a lightweight Mermaid-based browser page.

Open:

```text
index.html
```

The page can be used as a simple alternative for documenting smaller process flows.

## Local Usage

Clone the repository:

```bash
git clone https://github.com/fajarinsanfi-ops/FlowChart.git
cd FlowChart
```

For the basic browser flowchart, open:

```text
index.html
```

No build process is required.

## Deployment

The HTML/CSS portion can be deployed as a static website using GitHub Pages.

Recommended configuration:

```text
Branch: main
Folder: / (root)
```

The draw.io source remains available through the repository even when the browser preview is deployed separately.

## Documentation Guidelines

When adding a new flowchart:

1. Use a descriptive file name.
2. Keep the editable diagram source in the repository.
3. Add a preview link to the README.
4. Document the major systems and process steps.
5. Update the repository structure section.
6. Keep the README aligned with the actual process.

## Technology

| Technology | Purpose |
|---|---|
| draw.io / diagrams.net | Business process diagram |
| Mermaid | Lightweight flowchart rendering |
| HTML5 | Browser-based presentation |
| CSS3 | UI styling |
| GitHub | Source control and collaboration |

## Roadmap

Potential future improvements:

- Embedded diagram preview directly in the web page
- Interactive flowchart viewer
- Multiple flowchart catalog
- Diagram search and filtering
- PNG/SVG export
- Dark mode
- Version history per process
- Process documentation metadata
- Automated diagram preview generation
- GitHub Pages documentation site

## License

This repository currently has no explicit open-source license.

---

**Repository:** [fajarinsanfi-ops/FlowChart](https://github.com/fajarinsanfi-ops/FlowChart)
