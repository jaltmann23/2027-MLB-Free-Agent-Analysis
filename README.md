# 2027-MLB-Free-Agent-Analysis

# Analyzing the 2026-27 MLB Hitter Free Agent Class

An analysis of the 2026-27 MLB hitter free agent class using Statcast data.
It looks past 2026 results to expected stats, contact quality, and age to
decide which hitters teams should target and which they should avoid.

## Research Questions
1. Which free agent hitters over- or underperformed their expected stats in 2026?
2. Which free agent hitters have the underlying contact quality to sustain their production?
3. How does age affect the risk of signing each player?

## Key Findings

**Players to target**
- **Bo Bichette (3B/SS, 28):** expected stats well above actual results, high sweet spot %, and young
- **Jake Bauers (1B, 31):** highest barrel % and bat speed in the class
- **Trent Grisham (OF, 30):** one of the largest gaps between expected and actual production, with strong contact quality

**Players to avoid**
- **Randy Arozarena (OF, 31):** results ran well ahead of his expected stats, without elite bat speed or barrel % behind them
- **Ty France (1B, 32):** largest negative gap between xwOBA and wOBA in the class (about -0.04)
- **Paul Goldschmidt (1B/DH, 39):** results above expected stats, low exit velocity, and the age risk of a 39-year-old

## Data
- **Free agent list:** mlbtraderumors.com, typed into `mlb_free_agents_2026_27.csv`
- **Performance data:** Baseball Savant (Statcast) 2026 season, pulled with `pybaseball`
  (expected stats, bat tracking, exit velocity and barrels)
- **Scope:** qualified hitters only; no pitchers or defensive metrics

## Methods
- Matched each free agent to their MLB ID and merged the Statcast tables
- Calculated `xwOBA - wOBA` to measure over- and underperformance
- Visualized actual vs. expected wOBA and AVG, barrel % vs. bat speed, and exit velocity vs. sweet spot %

## Tools
Python, pandas, NumPy, matplotlib, seaborn, pybaseball, Jupyter Notebook

## Limitations
- One season of data, so lucky or unlucky years carry a lot of weight
- Hitters only; no defense or contract cost
- Age analysis is descriptive and can't predict how individual players will age
- Hitters without enough tracked swings were excluded

## Next Steps
- Add multiple seasons to see whether expected-vs-actual gaps persist
- Include pitchers and defensive metrics
- Add contract estimates and team needs

*By Joseph Altmann*
