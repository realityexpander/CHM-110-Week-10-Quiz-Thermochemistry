# CHM-110 Week 10 — Gases & Thermochemistry Quiz

A single-page, two-stage chemistry practice app for **CHM-110 Week 10: gas laws, stoichiometry, calorimetry, enthalpy, and thermochemistry**.

Each exercise first asks you to **identify the correct equation or conversion path** (multiple choice), then requires you to **type the final answer with the correct significant figures**. Incorrect attempts provide hints, and complete solutions show the dimensional-analysis setup **with units**.

**Version:** v2 — platform-specific hotkey hints and selected Stage 1 equation shown above Stage 2.

**Live source:** [CHM-110-Week-10-Quiz-Thermochemistry](https://github.com/realityexpander/CHM-110-Week-10-Quiz-Thermochemistry)

## Features

- **14 question families** modeled on a CHM-110 Week 10 practice quiz. One randomized instance of each appears per 14-question round; the order is shuffled again each round.
- **Two stages per question:** (1) select the correct equation/method; (2) see the selected equation displayed above Stage 2 and enter a numerical answer, or type the classification for conceptual questions.
- **Randomized values and presentation:** mass (g/kg), volume (L/mL), pressure (atm/Torr), temperature (°C/K), heat (J/kJ), enthalpy signs, and balanced-reaction scaling where applicable.
- **Significant-figure validation:** the numeric value and the count of significant figures are checked separately. Scientific notation such as `5.50e3` is accepted.
- **Units Mode:** OFF displays the expected unit beside the answer field; ON requires selecting the correct unit from a pop-up with **at least four options** after the numeric answer is right.
- **Unlimited retries**, escalating hints, **Skip**, **Show answer**, and **Show solution**.
- **Dimensional-analysis solutions**, including chemical mole ratios and explicit factor-label units.
- **Correct, Incorrect, Accuracy, Streak, and Best Streak** scorekeeping. Results persist in the browser's local storage and can be reset.
- **Dark and light themes**, responsive layout, keyboard shortcuts with platform-aware button/help labels (`Opt+` on Mac or `Alt+` on Windows), and LaTeX rendering via MathJax.
- **No build tools, framework, installation, backend, or account required.** The application is one HTML file.

## Topics / question families

| # | Topic | Recognition / method |
|---|---|---|
| 1 | Combustion, reactant mass → product gas volume | Grams → moles → reaction coefficients → `V = nRT/P` |
| 2 | Sodium with water, gas at STP | Grams → moles → mole ratio → `22.4 L/mol` |
| 3 | Reaction enthalpy sign | Positive ΔH = endothermic; negative ΔH = exothermic |
| 4 | Calorimetry: find sample mass | `m = q/[c(Tf − Ti)]` |
| 5 | Molar enthalpy of solution | `ΔHsoln = q/(mass/molar mass)` |
| 6 | Energy diagram / endo-exo concepts / specific heat | Compare energies, signs, and definitions |
| 7 | Gas product volume → solid reactant mass | `n = PV/RT` → mole ratio → molar mass |
| 8 | Reaction enthalpy sign | Endothermic or exothermic classification |
| 9 | Ideal Gas Law: pressure | `P = nRT/V` |
| 10 | Thermochemical reaction: energy → grams | kJ → moles via reaction ΔH → grams |
| 11 | Molecules → gas volume | Avogadro's number → `V = nRT/P` |
| 12 | Gas P/V/T → gas mass | `m = PVM/(RT)` |
| 13 | H₂ at STP → energy released | Liters → moles → reaction kJ |
| 14 | Cooling water: signed heat | `q = mc(Tf − Ti)` |

## Run locally

1. Download [`index_v2.html`](index_v2.html) (or the deployment-ready `index.html` from the ZIP).
2. Double-click the file to open it in a modern browser; alternatively, serve it with a small static server.
3. Allow access to the internet so MathJax can render the LaTeX mathematics.

All quiz logic is embedded in the single HTML file. The only external runtime resource is MathJax, loaded from a CDN.

## Deploy on GitHub Pages

1. Create (or open) the repository **`realityexpander/CHM-110-Week-10-Quiz-Thermochemistry`**.
2. Upload `index.html` from the ZIP to the root of the default branch (`main`). This is the deploy-ready copy of `index_v2.html`. Upload this `README.md` alongside it. You can also keep `index_v2.html` in the repository for version history.
3. In the repository, navigate to **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose `main` and `/ (root)`, then save.
6. After GitHub Pages finishes publishing, the app will typically be at:

   `https://realityexpander.github.io/CHM-110-Week-10-Quiz-Thermochemistry/`

The address above is the *expected* Pages URL, not a claim that Pages is already configured or live.

## How scoring works

- **Correct:** both stages solved without a wrong attempt, hint, skip, or answer reveal.
- **Incorrect:** the first wrong attempt or hint/reveal/skip for a question counts one miss. Additional retries do **not** add more misses for that question.
- A question solved after an error is still educationally completed, but does not become a first-try correct answer.
- **Accuracy** = `Correct / (Correct + Incorrect) × 100%`.
- **Streak** increments on consecutive first-try correct questions; a miss resets the streak.
- Score, best streak, theme, and Units Mode settings are saved in browser local storage. Use **Reset score** to erase the score only.

## Keyboard shortcuts

| Key | Action |
|---|---|
| `1`–`4` | Select one of four formula choices (stage 1) |
| `Enter` | Check typed answer or move to next question after completion |
| `Alt+H` (Windows) / `Option+H` (Mac) | Hint |
| `Alt+S` / `Option+S` | Skip |
| `Alt+A` / `Option+A` | Show answer |
| `Alt+R` / `Option+R` | Show complete solution |
| `Alt+N` / `Option+N` | Next question; skips unfinished question |
| `Alt+U` / `Option+U` | Toggle Units Mode |

While the unit-selection pop-up is open, choose its first four/five options with numeric keys.

## Chemical conventions and grading

- **STP:** uses the course convention of **0°C, 1 atm, 22.4 L/mol** for an ideal gas.
- **Ideal Gas Law constant:** `R = 0.08206 L·atm/(mol·K)`.
- **Pressure conversion:** `760 Torr = 1 atm`.
- **Temperature conversion:** `T(K) = T(°C) + 273.15`.
- **Avogadro's constant:** `6.02214076 × 10^23 mol⁻¹`.
- The application uses **3 significant figures** for each randomized final numerical answer, with input values formatted to support that precision. Conversion factors and formula coefficients are treated as exact.
- For ambiguous trailing zeros in an integer, use explicit scientific notation such as `5.50e3` for 3 significant figures.
- Signed energy (`q`) is negative if the sample releases heat; reaction questions asking *how much energy is released* expect the positive magnitude.
- Chemical equations are balanced. Whole-number scaling of all reaction coefficients is accompanied by matching scaling of reaction enthalpy.

**Important:** This is a study tool; thermodynamic and gas-law examples use idealized introductory-chemistry assumptions. It is not a substitute for your instructor's conventions or a graded assessment.

## Repository description (GitHub About)

> Interactive CHM-110 Week 10 gas laws and thermochemistry quiz: randomized two-stage questions, significant-figure checking, unit drills, keyboard shortcuts, and dimensional-analysis solutions.

## Attribution

©2026 Chris Athanas. [Link to source](https://github.com/realityexpander/CHM-110-Week-10-Quiz-Thermochemistry).
