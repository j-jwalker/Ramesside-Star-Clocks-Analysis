# Ramesside-Star_Clocks

The Ramesside Star Clocks (RSC) are ancient Egyptian astronomical tables painted 
into the tombs of Ramses VI, VII, and IX in the Valley of the Kings in Luxor, Egypt, 
dated to approximately 1100 BCE. Each clock consists of 24 bi-weekly tables tracking 
47 stars across one year, with 13 rows representing hours of the night and 7 columns 
representing positional subregions of the sky. The clocks were first documented and 
transcribed by Neugebauer and Parker (1960), whose work remains the foundational 
reference for RSC research. No surviving writings explain how or why the clocks were 
created, making their observational methodology an open research question.

This toolkit was developed to investigate that question computationally. By generating 
synthetic star clocks from adjustable observational parameters (random skies, the 
Hipparcos catalogue, or Sirius-based models) and statistically comparing them to the 
real RSC data, the code helps rule out candidate collection methodologies. The toolkit 
produces 8 statistical figures, a colour-coded frequency table, and 3 celestial map 
projections per run.

## Notebooks

| Notebook | Purpose |
|---|---|
| `StarData.ipynb` | Generates 8 statistical figures + 1 Excel frequency table from a run file |
| `MapMaker.ipynb` | Generates 3D and stereographic star maps from coordinates in degrees |
| `MapMaker (HH.MM.SS).ipynb` | Same as MapMaker but accepts RA in HH.MM.SS format |

## Outputs

**StarData** produces: star count figure, frequency by star, frequency by position, 
stars per table, average position & standard deviation, percentage star appearance, 
star stability chart (3D), and a position boxplot with t-test p-value.

**MapMaker** produces: 3D celestial sphere projection, stereographic northern 
hemisphere map, stereographic southern hemisphere map.

## Quick Start

### StarData
1. Place your run file (`.xlsx`) in the project folder
2. Open `StarData.ipynb` and set `file_path`, `sheet_name`, `runName`, and `series` 
   in the User Input section
3. Run all cells — output charts will appear in a new folder

### MapMaker
1. Place your coordinate file (`.xlsx`) in the project folder
2. Open the appropriate MapMaker notebook and set `file_path` and `Series`
3. Run all cells — 3 projection PNGs will appear in a new folder

## Dependencies
```bash
pip install pandas matplotlib scipy openpyxl numpy
```

## Full Documentation

See `Star Clocks Code Manual Jonah W.pdf` for detailed explanation of all outputs 
and code sections.

## References
Neugebauer, O. and Parker, R.A., 1960. *Egyptian Astronomical Texts*. Vol 2. 
Providence RI: Brown University Press.
