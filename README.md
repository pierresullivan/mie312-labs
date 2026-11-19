# MIE312 Fluid Mechanics I — Laboratory Manuals

LaTeX sources for the four laboratory manuals, and their companion Colab notebooks, used in MIE312 (Fluid Mechanics I), Department of Mechanical and Industrial Engineering, University of Toronto.

Each lab folder holds the manual (`main.tex`), its figures, and the companion Colab notebook used for the analysis.

| Lab | Folder | Topic | Notebook |
|-----|--------|-------|----------|
| 1 | [`lab1-flume`](lab1-flume) | Open Channel Flow | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/pierresullivan/mie312-labs/blob/main/lab1-flume/MIE312_Lab1_Open_Channel_Flow.ipynb) |
| 2 | [`lab2-pipe-losses`](lab2-pipe-losses) | Head Losses in Pipes and Fittings | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/pierresullivan/mie312-labs/blob/main/lab2-pipe-losses/MIE312_Lab2_Head_Losses.ipynb) |
| 3 | [`lab3-aero`](lab3-aero) | External Flow: Lift and Drag on Airfoils | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/pierresullivan/mie312-labs/blob/main/lab3-aero/MIE312_Lab3_External_Flow.ipynb) |
| 4 | [`lab4-turbines`](lab4-turbines) | Impulse Turbines: Application of Fluid Momentum Principles | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/pierresullivan/mie312-labs/blob/main/lab4-turbines/MIE312_Lab4_Impulse_Turbines.ipynb) |


## Download the PDFs

The latest compiled manuals are attached to the most recent [Release](https://github.com/pierresullivan/mie312-labs/releases/latest). Direct links (these always point to the newest version):

- [Lab 1 — Flume](https://github.com/pierresullivan/mie312-labs/releases/latest/download/MIE312_Lab1_Flume.pdf)
- [Lab 2 — Pipe Losses](https://github.com/pierresullivan/mie312-labs/releases/latest/download/MIE312_Lab2_Pipe_Losses.pdf)
- [Lab 3 — Aerodynamics](https://github.com/pierresullivan/mie312-labs/releases/latest/download/MIE312_Lab3_Aerodynamics.pdf)
- [Lab 4 — Turbines](https://github.com/pierresullivan/mie312-labs/releases/latest/download/MIE312_Lab4_Turbines.pdf)

## Using the notebooks

Click a badge above (or the link in the manual) to open the notebook in Google Colab, then choose **File → Save a copy in Drive** before entering data. Students work in their own copies; nothing they do changes this repository.

## Editing the notebooks

The notebooks in this repository are the master copies. To edit one in Colab, open it from its badge, make the changes, then use **File → Save a copy in GitHub** and commit back to the same path on `main` (untick *Include a link to Colaboratory*). Saved outputs are rejected by the build check, so before saving set **Edit → Notebook settings → Omit code cell output when saving this notebook**, or run **Edit → Clear all outputs**.

## Building locally

Each lab is self-contained: its `main.tex` and figure folder sit together. With a TeX Live installation:

```bash
cd lab1-flume
latexmk -pdf main.tex
```

To edit in Overleaf, upload a single lab folder as its own project (`main.tex` is the main document).

## Automated builds

Every push to `main` compiles all four manuals and runs every notebook top to bottom with GitHub Actions, so a broken notebook or manual is caught immediately; the PDFs are available under the workflow run's *Artifacts*. Publishing a Release (Releases → Draft a new release, with a tag such as `v2026.1`) attaches the compiled PDFs to it a few minutes later.

## License

© Pierre Sullivan, University of Toronto. All rights reserved unless a license is added.
