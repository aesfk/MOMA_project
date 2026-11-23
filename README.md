# Exploring the MoMA Collection

An exploratory data visualization project based on the Museum of Modern Art's public collection catalogue. It was completed for the 2025–2026 Scientific Data Visualization elective at HSE University.

## What the notebook explores

- **Artwork dates.** A histogram and smoothed yearly series show when the works in the catalogue were made. The plotted range is 1800–2025.
- **Recorded artist gender.** An area chart compares yearly artwork counts for records that the notebook recognizes as male or female. The counts describe artwork records, so an artist with several works can contribute several times.
- **Artwork dimensions.** A pictogram compares average size by decade. The size proxy uses a recorded diameter when available or the square root of width × height. The chart includes decades with at least ten usable records.
- **Artist nationalities.** A bar chart and a word cloud show frequencies among artist records with a usable nationality label.

## View or run the analysis

Open the [notebook](%D0%9F%D1%80%D0%BE%D0%B5%D0%BA%D1%82_MOMA.ipynb) to preview the saved charts. The repository also contains a [Russian-language overview PDF](%D0%9E%D0%B1%D0%B7%D0%BE%D1%80%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%9C%D0%9E%D0%9C%D0%90.pdf).

From the repository root, install the notebook dependencies and start Jupyter.

```bash
python -m pip install notebook numpy pandas matplotlib seaborn wordcloud
python -m jupyter notebook
```

Open the notebook and run all cells in order. It downloads `Artists.csv` and `Artworks.csv` from MoMA, so a fresh run needs an internet connection and uses the current catalogue. `MOMA_data_2022.csv` is a separate file bundled with the project. The notebook reads the upstream files. [MoMA collection data and CC0 terms](https://github.com/MuseumofModernArt/collection)

## How to read the charts

The figures describe MoMA's catalogued holdings. In a 23 November 2026 run, the parser extracted a year for 134,705 of 161,038 deduplicated artwork records (83.6%). The current parser skips some hyphenated date ranges. The dimension proxy supports an exploratory comparison across catalogue records with usable measurements.
