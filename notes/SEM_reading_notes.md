# SEM Paper-to-Slides Reading Notes

Source files read:

- `D:/Papers_PDF/Incoming/main.tex`
- `D:/Papers_PDF/Incoming/SEM0509.tex`

## Main Slide-Level Changes Needed

1. The main theorem should not be stated only on `R_{++}` without qualification.
   The paper works on `R_+`, uses parts of the nonnegative orthant, and then focuses on the strictly positive subset `\widetilde K = K \cap R_{++}^M`. Slides should say "at most one strictly positive fixed point/NE" unless the strategy space has strictly positive lower bounds.

2. The game theorem should say "strictly positive NE."
   The paper is careful about zero boundaries. Saying simply "at most one NE" is too strong unless boundary equilibria are ruled out.

3. Add a slide on primitive payoff characterization.
   The paper's Section "Characterization via utility functions" is important because it shows SEM is not only a best-response black box. The key slide formula should be:
   `SE_i^+(x_{-i}) = [sum_j |u_{ij}(x_i^*,x_{-i})| x_j] / [|u_{ii}(x_i^*,x_{-i})| x_i^*]`.

4. Comparative statics should emphasize "global" and "unit-free."
   The paper's comparative statics contribution is not just the feedback multiplier. It also gives global arc-elasticity bounds for finite parameter changes, unlike local IFT-style comparative statics.

5. For a 15-minute talk, keep one main application.
   Linear network games are the cleanest main application because they directly motivate the puzzle: large absolute network effects can coexist with weak relative feedback. CES/trade/linear-aggregator material should be backup or a brief "broader applications" slide.

6. The deck should keep the author's Beamer-design lessons but not copy the template literally.
   The full yellow transition screen felt inconsistent with the existing metropolis style. A subtle transition slide is better.

## Paper-Level Points Worth Checking

1. In `Application I: Linear best-responses`, the sentence defining strategic substitutes appears to say `g_{ij}\ge 0`; it likely should be `g_{ij}\le 0`.

2. Some copied text has encoding artifacts such as `player鈥檚`, `stability鈥攁n`, and `players鈥?prices`. These should be fixed before circulation.

3. The trade application states a uniqueness condition using `|alpha+beta-1| >= 1`. If the proof relies on a strict contraction, the weak equality case should be checked carefully. It may need a strict inequality or a separate argument for the boundary case.

4. The CES application is interesting, but for a short talk it may distract from the paper's central contribution unless the audience is especially IO/pass-through oriented.

5. The introduction's most compelling hook is the Belhaj et al. bounded-network puzzle. The slides should foreground that puzzle rather than begin with a broad literature tour.

## Deck Revision Made

The improved deck now:

- Uses the `R_+` / `\widetilde K` / strictly-positive wording.
- Adds the utility-characterization slide.
- Adds "global and unit-free" to comparative statics.
- Adds a backup slide for other applications.
- Softens transition slides to match the user's metropolis template.
