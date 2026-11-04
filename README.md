# CHM-110 Week 10 — Gases & Thermochemistry Quiz

A single-page, two-stage chemistry practice app for **CHM-110 Week 10: gas laws, stoichiometry, calorimetry, enthalpy, and thermochemistry**.

Each exercise first asks you to **identify the correct equation or conversion path** (multiple choice), then requires you to **type the final answer with the correct significant figures**. Incorrect attempts provide hints, and complete solutions show the dimensional-analysis setup **with units**.

**Version:** v4 — chemical-name-to-formula practice, five additional binary gases, alternating hot/cold-water examples, version/date-time footer, and expanded outcome-based scoring. The app's footer includes the local creation timestamp (Eastern Time).

**Live source:** [CHM-110-Week-10-Quiz-Thermochemistry](https://realityexpander.github.io/CHM-110-Week-10-Quiz-Thermochemistry/)

## Features

- **14 question families** modeled on a CHM-110 Week 10 practice quiz. One randomized instance of each appears per 14-question round; the order is shuffled again each round.
- **Gas formula practice:** question family 12 displays the compound **name only**. Derive its chemical formula from prefixes before finding molar mass. Hints and solutions reveal the formula when requested. Six compounds are included: dinitrogen trioxide (N₂O₃), dinitrogen monoxide (N₂O), nitrogen dioxide (NO₂), carbon dioxide (CO₂), sulfur dioxide (SO₂), and sulfur hexafluoride (SF₆).
- **Both heat-transfer directions:** water-heating examples are exothermic; water-cooling examples are endothermic. Whenever this question variant appears, its endothermic/exothermic answer alternates from the previous appearance.
- **Two stages per question:** (1) select the correct equation/method; (2) see the selected equation displayed above Stage 2 and enter a numerical answer, or type the classification for conceptual questions.
- **Randomized values and presentation:** mass (g/kg), volume (L/mL), pressure (atm/Torr), temperature (°C/K), heat (J/kJ), enthalpy signs, and balanced-reaction scaling where applicable.
- **Answer validation:** numerical answers within **±1.5%** of the unrounded expected result are accepted **only if the required significant-figure count also matches**. Accepts scientific notation such as `1.10x10^23`, `1.10*10^23`, `1.10×10^23`, and `1.10e23`. App displays scientific values as **6.31 × 10⁴** rather than `6.31e+4`.
- **Units Mode:** OFF displays the expected unit beside the answer field; ON requires selecting the correct unit from a pop-up with **at least four options** after the numeric answer is right.
- **Unlimited retries**, escalating hints, **Skip**, **Show answer**, and **Show solution**.
- **Dimensional-analysis solutions**, including the original **Stage 1 equation / selected method**, chemical mole ratios, and explicit factor-label units.
- **Six scoring cards:** Correct (first try), Correct after attempts, Incorrect (questions with wrong submissions), Skipped (including answer reveals), Percent Correct, and Streak/Best Streak. Results persist in browser storage and can be reset.
- After success, navigation is labeled **Next Question** and the separate Skip button is hidden. A solved problem that needed retries is labeled **Completed successfully after multiple attempts**.
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
| 6 | Energy diagram / endo-exo concepts / specific heat | Compare energies, signs, definitions, and hot/cold surrounding water |
| 7 | Gas product volume → solid reactant mass | `n = PV/RT` → mole ratio → molar mass |
| 8 | Reaction enthalpy sign | Endothermic or exothermic classification |
| 9 | Ideal Gas Law: pressure | `P = nRT/V` |
| 10 | Thermochemical reaction: energy → grams | kJ → moles via reaction ΔH → grams |
| 11 | Molecules → gas volume | Avogadro's number → `V = nRT/P` |
| 12 | Binary molecular gas name → formula → mass | Derive formula, compute molar mass, then `m = PVM/(RT)` |
| 13 | H₂ at STP → energy released | Liters → moles → reaction kJ |
| 14 | Cooling water: signed heat | `q = mc(Tf − Ti)` |

## Run locally

1. Download [`index_v4.html`](index_v4.html) (or the deployment-ready `index.html` from the ZIP).
2. Double-click the file to open it in a modern browser; alternatively, serve it with a small static server.
3. Allow access to the internet so MathJax can render the LaTeX mathematics.

All quiz logic is embedded in the single HTML file. The only external runtime resource is MathJax, loaded from a CDN.

## Deploy on GitHub Pages

1. Create (or open) the repository **`realityexpander/CHM-110-Week-10-Quiz-Thermochemistry`**.
2. Upload `index.html` from the ZIP to the root of the default branch (`main`). This is the deploy-ready copy of `index_v4.html`. Upload this `README.md` alongside it. You can also keep `index_v4.html` in the repository for version history.
3. In the repository, navigate to **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose `main` and `/ (root)`, then save.
6. After GitHub Pages finishes publishing, the app will typically be at:

   `https://realityexpander.github.io/CHM-110-Week-10-Quiz-Thermochemistry/`

The address above is the *expected* Pages URL, not a claim that Pages is already configured or live.

## How scoring works (v4)

- **Correct:** number of questions completed with both stages right **on the first attempt and without a hint**.
- **Correct after attempts:** number of questions eventually completed after any wrong submission or hint. Displays the message **Completed successfully after multiple attempts**.
- **Incorrect:** number of distinct questions for which **one or more wrong answers** were submitted; repeated wrong answers on the *same question* count just once. It is a diagnostic counter, so it can overlap with Correct after attempts or Skipped.
- **Skipped:** number of questions left unfinished by Skip/Skip to next; **Show answer / Show solution** before solving also counts as skipped. Once a question is complete, Next Question does **not** add to Skipped.
- **Percent Correct:** `(Correct + Correct after attempts) / (Correct + Correct after attempts + Skipped) × 100%`. This measures the share of finished questions that you solved, with or without retries. The Incorrect counter is not included separately because that would double count questions solved after a wrong attempt.
- **Streak:** consecutive first-try correct questions; a wrong answer, hint, skip, or reveal resets it. **Best Streak** records the longest streak.
- **Reset score** clears these counters. Scores use a new local-storage key for v4, so earlier v3 counts are not mixed into the new scoring model; theme and Units Mode preferences persist.

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
- The application uses **3 significant figures** for each randomized final numerical answer. The app checks both the **±1.5% relative numeric tolerance** and **exactly 3 significant figures**. Conversion factors and formula coefficients are treated as exact.
- Accepted notation: `1.10x10^23`, `1.10*10^23`, `1.10×10^23`, or `1.10e23`; output is rendered as **1.10 × 10²³**.
- Atomic masses (g/mol): **H = 1.01; C = 12.01; N = 14.01; O = 16.00** (specified CHM-110 values). Added gases also use **S = 32.06; F = 19.00**. The other derived masses are **butane 58.14; ammonium nitrate 80.06; acetic acid 60.06**.
- Gas-formula practice molar masses (g/mol): **N₂O₃ 76.02; N₂O 44.02; NO₂ 46.01; CO₂ 44.01; SO₂ 64.06; SF₆ 146.06**. All formulas are displayed only in hints/solutions, *not in the question prompt*.
- For ambiguous trailing zeros in an integer, use explicit scientific notation such as `5.50x10^3` for 3 significant figures.
- Signed energy (`q`) is negative if the sample releases heat; reaction questions asking *how much energy is released* expect the positive magnitude.
- Chemical equations are balanced. Whole-number scaling of all reaction coefficients is accompanied by matching scaling of reaction enthalpy.

**Important:** This is a study tool; thermodynamic and gas-law examples use idealized introductory-chemistry assumptions. It is not a substitute for your instructor's conventions or a graded assessment.

## Repository description (GitHub About)

> Interactive CHM-110 Week 10 gas laws and thermochemistry quiz: randomized two-stage questions, significant-figure checking, unit drills, keyboard shortcuts, and dimensional-analysis solutions.

## Compound name and formula references

Five extra binary compounds were selected using [OpenStax Chemistry 2e, chemical nomenclature](https://openstax.org/books/chemistry-2e/pages/2-7-chemical-nomenclature), [NIST Chemistry WebBook (dinitrogen monoxide)](https://webbook.nist.gov/cgi/cbook.cgi?ID=C10024972&Mask=800), and PubChem entries for [carbon dioxide](https://pubchem.ncbi.nlm.nih.gov/compound/carbon_dioxide), [nitrogen dioxide](https://pubchem.ncbi.nlm.nih.gov/compound/Nitrogen-Dioxide), [sulfur dioxide](https://pubchem.ncbi.nlm.nih.gov/compound/sulfur-dioxide), and [sulfur hexafluoride](https://pubchem.ncbi.nlm.nih.gov/compound/sulfur_hexafluoride).

These are **ideal-gas classroom exercises**, not predictions of real equilibrium gas mixtures. For example, nitrogen dioxide can form an equilibrium mixture with dinitrogen tetroxide, and dinitrogen trioxide is an idealized example at typical conditions.

## Version history

- **v4:** Hides formulas in named-gas questions; adds five researched binary compounds; alternates heat-absorbing and heat-releasing water scenarios; adds footer version timestamp; changes successful navigation to **Next Question**; displays **Completed successfully after multiple attempts**; and adds **Correct after attempts** and **Skipped** counters.
- **v3:** Added typed `x10^` and `*10^` scientific notation; readable multiplication-sign/exponent output; updated H/C/N/O atomic masses; ±1.5% numerical tolerance combined with significant-figure validation; and the Stage 1 equation at the beginning of Show Solution.
- **v2:** Automatic `Opt+`/`Alt+` labels and selected equation displayed above Stage 2.
- **v1:** Initial randomized two-stage 14-question quiz.

## Attribution

©2026 Chris Athanas. [Link to source](https://github.com/realityexpander/CHM-110-Week-10-Quiz-Thermochemistry). The app footer adds the creation version/date/time stamp immediately after this link.
