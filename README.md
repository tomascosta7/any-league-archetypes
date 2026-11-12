# Any League? Probabilistic Player Archetypes in Women's Basketball

Replication of *Scouting Anyone: Probabilistic Player Archetypes for Any League* (Myrte, Buzzalino and Aymerich, MIT Sloan Sports Analytics Conference 2026) on the Spanish **Liga Femenina Endesa**.

**Tomás Costa** · MSc in Sports Analytics · Escuela Universitaria Real Madrid – Universidad Europea · November 2026

**Paper:** [paper/Any_League_Costa_2026.pdf](paper/Any_League_Costa_2026.pdf)

## Key findings

- Archetypal Analysis on 15 box-score features finds **eight archetypes** in 142 player-team stints (2025/26), explaining **69.5%** of the variation (K-Means: 49.6%).
- **Role players come in types, stars don't:** stability across 20 refits falls with usage (r = −0.81), from 89% (Spot-Up Shooter) to 26% (Scoring Wing).
- The paper's **role-player archetypes transfer** to the women's game (Traditional Playmaker ↔ Floor General, 3PT Specialist ↔ Spot-Up Shooter); the **interior and creators are organised differently**, and the Combo Creator has no men's counterpart.
- Projected to 2026/27 with the frozen model, **30% of players change role beyond a noise baseline** that only 10% would exceed by chance.

## Repository

| Path | Content |
| --- | --- |
| `01_dados.ipynb` | Scraping and validating the data from the FEB website (two seasons) |
| `02_model.ipynb` | Features, Archetypal Analysis, stability, KNN, 2026/27 projection and noise baseline |
| `03_results.ipynb` | Archetype portraits, team fingerprints, player cards, PCA map, comparison with the paper |
| `figures/` | All figures, 142 player cards (`player_cards/`) and interactive Plotly maps (`plotly/`) |
| `paper/` | The paper (PDF) |
| `environment.yml` | Conda environment |

The notebooks are kept as a learning record: **errors and their fixes are left visible**, each followed by a note and the corrected cell. *Run All* therefore stops at the first intentional error; run the cells in order instead.

## How to reproduce

    conda env create -f environment.yml
    conda activate liga_femenina
    jupyter lab

Then run `01_dados.ipynb`, `02_model.ipynb` and `03_results.ipynb`, in that order.

## Data

Data come from the official website of the Spanish Basketball Federation, [baloncestoenvivo.feb.es](https://baloncestoenvivo.feb.es). **The scraped data are not included in this repository**; `01_dados.ipynb` regenerates them (with a one-second pause between requests). The 2025/26 box scores of Movistar Estudiantes miss 372 points at the source; see the paper for details.

This is an independent academic project, not affiliated with the FEB or the Liga Femenina Endesa.

## Citation

> Costa, T. (2026). *Any League? Probabilistic Player Archetypes in Women's Basketball.* MSc in Sports Analytics, Escuela Universitaria Real Madrid – Universidad Europea.
