# 🏀 NBA Matchup Analyzer

A Python command-line tool that pulls real NBA game data and breaks down how any team historically performs against a specific opponent — across offense, defense, and rebounding.

## What It Does

Given two NBA team abbreviations and a season year, the tool:
- Fetches all games played by the first team that season via the NBA Stats API
- Filters for games played against the second team
- Compares performance in those matchups vs the team's overall season averages
- Outputs a structured scouting report with an offensive, defensive, rebounding, and overall verdict

## Sample Output

=== Matchup Analysis vs MIA ===
OFFENSE:

Scoring: Score MORE vs MIA (114.5 vs 108.2 avg) — favorable offensive matchup


Shooting: Shoot LESS efficiently vs MIA (0.441 vs 0.463 avg)

= Turnovers: About the same turnover rate vs MIA (13.1 vs 13.4 avg)

DEFENSE:

Steals: More active hands vs MIA (8.2 vs 7.1 avg) — force more turnovers

= Blocks: About average rim protection vs MIA (4.8 vs 4.9 avg)

REBOUNDING:

Rebounds: Get out-rebounded by MIA (41.2 vs 44.3 avg)

= Off. Rebounds: About average second chances vs MIA (9.8 vs 10.1 avg)

OVERALL:

Plus/Minus: Tend to WIN vs MIA (avg +/- +4.2)

VERDICT:

Offensive edge vs MIA, but defense is a concern.

## Tech Stack

- **Python 3**
- [`nba_api`](https://github.com/swar/nba_api) — unofficial NBA Stats API wrapper
- `pandas` — data filtering and aggregation

## Setup

```bash
# Clone the repo
git clone https://github.com/JackZhhhh/nba-matchup-analyzer.git
cd nba-matchup-analyzer

# Install dependencies
pip install nba_api pandas

# Run
python main.py
```

## Usage

You'll be prompted for:
1. **Home team abbreviation** (e.g. `BOS`, `LAL`, `GSW`)
2. **Season year** (e.g. `2024` for the 2024–25 season)
3. **Opponent abbreviation**

## Metrics Analyzed

| Category | Metrics |
|---|---|
| Offense | Points, FG%, Turnovers |
| Defense | Steals, Blocks |
| Rebounding | Total Rebounds, Offensive Rebounds |
| Overall | Plus/Minus |

## Future Plans

- [ ] Add player-level breakdowns
- [ ] Win probability prediction model
- [ ] Web frontend with charts and visualizations
- [ ] Support for multi-season trend analysis
