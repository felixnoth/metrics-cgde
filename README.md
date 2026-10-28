# Econometrics (PhD) — CGDE / IWH Halle

Companion repository for the first-year Econometrics course of the
[Central-German Doctoral Program in Economics (CGDE)](https://cgde-home.de),
hosted at the Halle Institute for Economic Research (IWH) and taught by
[Felix Noth](https://felixnoth.github.io). Course page with schedule and
organization:
[felixnoth.github.io/teaching/econometrics-phd](https://felixnoth.github.io/teaching/econometrics-phd.html).

Support material lives here as Jupyter notebooks — one folder per session.
Notebooks are committed with executed output, so you can read them directly
on GitHub before running anything yourself.

## Sessions

| Folder | Content |
|--------|---------|
| `session-01-ols/` | OLS by matrix algebra: derivation, a small worked example, the variance-covariance matrix, standard errors, a Monte Carlo look at the sampling distribution, and the Frisch–Waugh–Lovell theorem (regression anatomy). |
| `session-02-logs/` | Logs in regressions: elasticities, exact vs. approximate interpretation of log coefficients, the log base 1.1 trick, and why `log(1+Y)` / `arcsinh(Y)` fail with zeros — with the unit-invariant alternatives (two-part margins, levels OLS, Poisson). |
| `session-03-interactions/` | Interaction effects: what the coefficients mean, marginal effects with delta-method standard errors over the moderator, the Brambor–Clark–Golder checklist, binary × binary (the DiD shape), centering, and the "16 times" power rule. |
| `session-04-good-bad-controls/` | Good and bad controls: regression anatomy revisited, nine simulated worlds (confounder, mediator, collider, M-bias, bias amplifier, …) with one estimator, a collider you can derive (the budget deficit), why coefficient movement is not a diagnostic, when a control is needed at all (Cunningham), Gelbach's decomposition and Oster's δ. |
| `session-05-fixed-effects/` | Fixed effects and standard errors: within vs. between variation, dummies vs. demeaning (degrees-of-freedom correction), two-way FE, a Petersen-style Monte Carlo on clustered standard errors with a constant unit effect and with serially correlated (AR(1)) idiosyncratic components on top of it, when clustering hurts and when it does not (Abadie et al.), and the incidental-parameters problem in a fixed-effects logit. |
| `session-06-iv/` | Instrumental variables: Wald, covariance ratio and 2SLS by hand; a weak-instrument Monte Carlo (bias toward OLS, t-based coverage vs. the Anderson–Rubin confidence set, constructed by test inversion — bounded when the instrument is strong, the whole line when it is not); many weak instruments (and why the joint first-stage F is not the diagnostic); LATE with compliers, always- and never-takers; a judge-leniency simulation with a leave-one-out instrument, judge-clustered inference, and a monotonicity violation. |

Sessions 1–3 accompany lecture AE1.1 (Regression Review I and II), session 4
accompanies AE1.2 (Causality and Potential Outcomes I), session 5 accompanies
AE1.3 (Fixed Effects and Standard Errors), session 6 accompanies AE1.4
(Instrumental Variables I and II). More sessions are
added over the term.

## Readings

The course draws on Huntington-Klein (2025), *The Effect*, 2nd ed. — free at
[theeffectbook.net](https://theeffectbook.net) — and Cunningham (2026),
*Causal Inference: The Mixtape*, 2nd ed. (online edition; chapter and section
numbers in the notebooks refer to the version online in October 2026) — free at
[mixtape.scunning.com](https://mixtape.scunning.com); the regression review
uses the 1st edition's chapter 2, which stays online at
[mixtape-1ed.netlify.app](https://mixtape-1ed.netlify.app) — plus papers
announced per session.

## Getting started

1. Install Python 3.11+ ([python.org](https://www.python.org) or
   [Anaconda](https://www.anaconda.com/download)).
2. Create an environment and install the course stack:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate            # Windows: .venv\Scripts\activate
   pip install -r requirements.txt
   python -m ipykernel install --user --name metrics-cgde --display-name "Python (metrics-cgde)"
   ```

3. Download this repository (green **Code** button → Download ZIP, or
   `git clone https://github.com/felixnoth/metrics-cgde.git`) and open the
   session notebook in VS Code or JupyterLab.

## License

MIT — see `LICENSE`.
