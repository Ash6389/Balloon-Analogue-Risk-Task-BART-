# BART Balloon Game

A browser version of the **Balloon Analogue Risk Task (BART)**, recreated from the balloon game used in this study:

> Pei, R., Lauharatanahirun, N., Cascio, C. N., O'Donnell, M. B., Shope, J. T., Simons-Morton, B. G., Vettel, J. M., & Falk, E. B. (2020). Neural processes during adolescent risky decision making are associated with conformity to peer influence. *Developmental Cognitive Neuroscience, 44*, 100794. https://doi.org/10.1016/j.dcn.2020.100794

In the study, 83 adolescent males (16 to 17 years old) played the BART inside an fMRI scanner. One week later they drove a driving simulator, alone and with a peer passenger who encouraged either risky or safe driving. Brain activity that scaled with the stakes in the balloon game predicted who followed the risky peer.

This project recreates that balloon game so a class can play it together and compare their own risk taking with the teenagers in the study.

**Play online:** `https://YOUR-USERNAME.github.io/YOUR-REPO/` (replace this with your GitHub Pages link)

---

## How to play

1. Enter your name, choose the number of balloons and the timing, then press **Start game**.
2. Press **Inflate** (or the Space key) to pump the balloon. Each pump makes it bigger and raises its wager.
3. Press **Bank** (or the Enter key) to add the wager to your total. Banked points are safe.
4. If the balloon explodes before you bank, you lose that balloon's wager.
5. Bigger balloons are worth more, but they are also more likely to explode. Try to finish with as many points as possible.

---

## What stays the same as in the paper

| Feature | In this game |
| --- | --- |
| Choices | Inflate or Bank on every step, as in the study |
| Maximum pumps per balloon | 12 |
| Balloon value | Rises from 0 to 5.15 points. The first pumps are worth 0.05, 0.15 and 0.25, as shown in Figure 1 of the paper |
| Screen | Shows "Wager" and "Total" under the balloon, then "Success!" or "Fail!" after each balloon, as in Figure 1 |
| Lab timing | Random 1.5 to 2.5 s pause between decisions on the same balloon, and 2 to 4 s between balloons |
| Risk measure | Adjusted pumps: the average number of pumps on balloons that were banked (not exploded) |
| Other measures | Balloons banked, balloons exploded, and average decision time for Inflate and for Bank |

---

## What we changed and improved

### 1. Choose how long the game lasts
The paper used fixed scanner runs, and participants completed about 28 balloons on average. Here the teacher or player can choose **30 balloons** (full task), **20** (shorter) or **10** (a quick turn), so the game fits into any lesson.

### 2. Choose the timing
**Lab timing** keeps the pauses from the scanner study. **Quick play** uses short pauses, which is better when many students need a turn.

### 3. Explosions are much harder to predict
In the paper's schedule, the chance of bursting climbs steeply with every pump (up to 89.6% on the 12th pump). As a result, most balloons burst within a narrow range of sizes, and players quickly learn to stop at about the same wager.

In this version:

- Each balloon has a hidden burst point somewhere between pump 3 and pump 12.
- A balloon never bursts on the first two pumps, so it never pops while it is still tiny.
- About 1 in 10 balloons never bursts and can be pumped all the way to full size.
- Burst points are spread across the whole range for each game and then shuffled, so they do not bunch up around one size or one wager.
- Bigger balloons are still riskier: the chance that the next pump bursts an intact balloon rises from 4% (pump 3) to 44% (pump 12).

### 4. A balloon that feels real
- The balloon grows with an elastic, rubbery motion.
- Explosions throw rubber pieces across the screen, with a "POP!" burst and a short screen shake.
- Banked balloons float away, and the points fly into your total.
- All sounds (air pump, pop, coin) are generated in the browser. No sound files are needed.

### 5. Instant results for discussion
At the end, each player sees:
- Total points, adjusted pumps, balloons banked and exploded, and decision times.
- Where their adjusted pumps fall compared with the study's participants (mean 4.70, SD 0.86).
- The hidden payoff chart: the average points per balloon for each stopping point. On average, banking after 8 pumps earns the most. This makes a good starting point for a class discussion about risk.

### 6. Classroom tools
- **Class board:** every finished game is saved and ranked on the computer it was played on. This works well when the class takes turns on one projected computer.
- **Copy table for Excel / Sheets:** copies the whole class board, ready to paste into a spreadsheet.
- **Copy my result:** copies a one-line summary that students can paste into a class chat when each student plays on their own device.
- **Copy balloon data:** copies balloon-by-balloon data (pumps, outcome, points, decision time) for analysis.

### 7. Works anywhere
- One single HTML file. No server, no installation, no account.
- Works on computers, tablets and phones, with keyboard shortcuts, a full-screen button and a dark mode.

---

## Burst schedule used in this game

| Pump | Wager after this pump | Chance this pump bursts an intact balloon | Share of balloons that burst on this pump | Average points if you always bank after this pump |
| --- | --- | --- | --- | --- |
| 1 | 0.05 | 0% | 0% | 0.05 |
| 2 | 0.15 | 0% | 0% | 0.15 |
| 3 | 0.25 | 4% | 4% | 0.24 |
| 4 | 0.55 | 7% | 7% | 0.49 |
| 5 | 0.95 | 10% | 9% | 0.76 |
| 6 | 1.45 | 13% | 10% | 1.01 |
| 7 | 2.05 | 16% | 11% | 1.21 |
| 8 | 2.75 | 19% | 11% | **1.32** |
| 9 | 3.45 | 23% | 11% | 1.28 |
| 10 | 4.25 | 27% | 10% | 1.15 |
| 11 | 4.70 | 33% | 9% | 0.85 |
| 12 | 5.15 | 44% | 8% | 0.52 |

The remaining 10% of balloons never burst. Players are not shown this table before they play.

---

## Put it on GitHub Pages

1. Create a public repository and upload `index.html` (keep this exact file name) and `README.md`.
2. Go to **Settings > Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select the `main` branch and the `/ (root)` folder, then save.
4. After a minute or two, the page shows your link, for example `https://your-username.github.io/your-repo/`. Share it with your class.

You can also open `index.html` directly by double-clicking it. It works offline too.

---

## Privacy

Everything runs in the player's browser. Nothing is sent to a server. The class board is stored only in the browser on the computer where the games were played, and can be cleared at any time with **Clear board**.

---

## Notes and limitations

- Because the burst schedule is different from the study's, scores in this game are not directly comparable with the paper's results. Treat the comparison as a rough guide.
- In the study, points were converted into money. Here points have no money value, which may make players take more risks.
- The instructions keep the paper's wording ("the balloon could explode at any size"), even though in this version the first two pumps are always safe.
- The paper reports only the start and end of the wager schedule and the first steps shown in Figure 1. The wager values in between are our reconstruction.
- This is an educational project and is not affiliated with the authors of the study.
