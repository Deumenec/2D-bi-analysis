# 2D-Bi STML Analysis

Data and analysis code accompanying the Bachelor's thesis:

**Optical response from bidimensional bismuth layers studied by Scanning Tunneling Luminescence**  
Domènec Huerta Estradé — Universitat Autònoma de Barcelona & ICN2, 2026

---

## Repository contents

```
├── June 2026/                     # Raw experimental session data
│   ├── Ag(111)_*.sxm              # Nanonis topographic images of clean Ag(111)
│   ├── Bi_Ag(111)_*.sxm          # Topographic images after Bi deposition
│   ├── *.dat                      # Nanonis point spectroscopy files (plain text)
│   └── *.hdf5 / *.h5              # HDF5/NeXus output from INSTANT
├── plots/                         # Generated figures
├── stml_analysis.ipynb            # Main analysis notebook
├── requirements.txt               # Python dependencies
└── LICENSE
```

## Data formats

| Extension | Description |
|---|---|
| `.sxm` | Nanonis topographic image (binary). |
| `.dat` | Nanonis point spectroscopy file (plain text). |
| `.hdf5` / `.h5` | HDF5/NeXus output from INSTANT (see thesis Appendix D). Contains raw spectra, scan axes, and full pre/post-acquisition instrumental metadata (bias, current, tip position, detector temperature, spectrometer configuration). |

## Running the analysis

Requires Python 3.10 or later. Install dependencies and launch the notebook:

```bash
python3 -m venv env
source env/bin/activate          # on Windows: env\Scripts\activate
pip install -r requirements.txt
jupyter lab stml_analysis.ipynb
```

All figures used in the thesis are reproducible from `stml_analysis.ipynb`.
Processed outputs are saved to `plots/`.

## Experimental conditions

All data were acquired with a Nanonis Mimea low-temperature STM operating
at T ≈ 77 K and base pressure below 10⁻¹⁰ mbar. Bismuth was deposited by
electron-beam evaporation from a high-purity Bi rod. STML spectra were
recorded and processed with the INSTANT acquisition software (Appendix D
of the thesis). Full sample preparation parameters and acquisition settings
are given in the Methods section of the thesis.

## Citation

If you use this data or code, please cite:

> D. Huerta Estradé, *Optical response from bidimensional bismuth layers
> studied by Scanning Tunneling Luminescence*, Treball de Fi de Grau en
> Física, Universitat Autònoma de Barcelona, 2026.

## License

Data and analysis code are released under the
[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE) licence.
You are free to share and adapt the material for any purpose, provided
appropriate credit is given.
