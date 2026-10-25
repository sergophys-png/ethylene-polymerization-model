# Two-Moment Kinetic Model of Ethylene Polymerization

Python code for a two-moment kinetic model of ethylene polymerization.
Accompanies the manuscript.

State: y = [C, N, P, M, H, Ps, Ns] — catalyst centers, growing chains,
incorporated monomer units, monomer, hydrogen, polymer units, terminated chains.

Parameters: alpha, beta, gamma, eps, eta (dimensionless groups).

Invariants: M + P + Ps = 1, C + N + Ns = 1.

## Requirements
Python 3.8+, numpy, scipy, matplotlib.

## Run
python script.py

Output goes to out/: listing.txt, table1.tex, report.json, sweep*.csv, single_III.pdf.

## Method
Implicit Radau (solve_ivp, rtol=1e-10, atol=1e-13). Extrema via event detection;
maximum of L = P/(eps*N) via root-finding. Cross-checked against RK45 and tighter tolerance.

## Citation
Please cite the accompanying manuscript.

## License
MIT
