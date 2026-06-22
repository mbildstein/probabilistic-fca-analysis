# Probabilistic FCA Analysis

A research and modeling toolkit for introducing probabilistic
cost estimation into Facility Condition Assessment (FCA)
workflows. This project explores methods for quantifying
uncertainty in renewal cost forecasts, moving beyond
deterministic point estimates toward confidence-aware capital
planning outputs.

## Background

Standard FCA practice produces single-point cost estimates
for component renewals, typically derived from unit cost
databases applied to observed quantities. While useful for
budgeting, these estimates carry implicit uncertainty that is
rarely made explicit — uncertainty in unit costs, service
life assumptions, condition score interpretation, and
escalation rates compounds across a portfolio.

This project investigates whether probabilistic methods can
produce more defensible cost ranges for FCA deliverables,
particularly for long-horizon capital planning and
portfolio-level risk assessment.

## Methodology

The primary technique under investigation is Monte Carlo
simulation, in which key input variables (unit costs,
remaining useful life, escalation rates) are treated as
probability distributions rather than fixed values. By
running many simulations across these distributions, the
model produces a range of plausible cost outcomes rather
than a single estimate.

This methodology is being developed in a municipal
facilities context, with ASTM Uniformat II as the
classification framework and FCI/BCA metrics as the
primary outputs.

> **Status:** Early-stage and exploratory. Core methodology
> is still being defined. Do not use outputs for client
> deliverables without review.

## Project Structure
To be developed.

## Data

Input data follows ASTM Uniformat II component structure
with associated quantities, unit costs, condition scores,
and service life estimates. Source data is derived from
actual facility assessments and is excluded from this
repository for confidentiality reasons.

Any sample or anonymized datasets used for development and
testing will be stored in `data/sample/` and committed to
the repo.

## Requirements

- Python 3.10+
- PostgreSQL (via WSL)
- See `requirements.txt` for Python package dependencies

## Setup

1. Clone the repository:
   `git clone https://github.com/mbildstein/probabalistic-fca-analysis.git`
2. Create and activate a virtual environment:
   `python -m venv venv && source venv/bin/activate`
3. Install dependencies:
   `pip install -r requirements.txt`
4. Configure your database connection in `.env`
   (see `.env.example` if provided)

## Usage

Open the notebooks in `notebooks/` sequentially. Entry point and workflow documentation
will be added as the methodology stabilizes.

## Status

Early / exploratory. Core probabilistic methodology is
under active research. Structure, outputs, and interfaces
are subject to significant change.

## License

Internal use only. Not licensed for external distribution.
