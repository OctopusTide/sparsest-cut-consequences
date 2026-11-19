# Consequences of constant-factor hardness for uniform sparsest cut

This repository holds a paper deriving NP-hardness of approximation for treewidth, bicliques, dense subgraphs and small-set expansion from OpenAI's September 2026 theorem that Uniform Sparsest Cut is NP-hard to approximate within every constant factor.

The statements and proofs were generated mainly by AI systems, and each transfer was checked by independent AI referees. See the section "Use of AI" of the paper.

Paper: [`paper/sparsest_cut_consequences.pdf`](paper/sparsest_cut_consequences.pdf) (26 pages). Article: [anaphos.com/sparsest-cut](https://anaphos.com/sparsest-cut).

## Main results

All results are deterministic polynomial-time reductions from 3SAT. They take as given the weighted cut gap in the proof of OpenAI's preprint ([Constant-factor hardness of uniform sparsest cut](https://github.com/openai/math/tree/main/preprints/Constant-factor-hardness-of-uniform-sparsest-cut-September-24-2026), September 24, 2026; Theorem 6.1, Proposition 7.1 and §8.1), called Theorem U in the paper. That preprint is not peer reviewed, and all results below are conditional on it.

- **Treewidth family.** For every fixed $c>1$ it is NP-hard, on simple bipartite graphs, to distinguish treedepth at most $s$ from treewidth greater than $cs$. Hence treewidth, pathwidth, treedepth and minimum fill-in are NP-hard to approximate within every constant factor. The same holds for branch-width, maximum-matching width, cutwidth, minimum linear arrangement and the other vertex and edge layout objectives, carving-width, interval completion, one-shot black and black-white pebbling, minimum bisection, balanced edge and vertex separators, and min-sum and min-max balanced $k$-partitioning; and, on line graphs of bipartite graphs, for clique-width, NLC-width, rank-width, Boolean-width, mim-width and tree-independence number.
- **Small-set expansion.** For every fixed rational $0<\delta\le 1/4$ there are $d$ and $\eta<1/2$ such that it is NP-hard, on simple bipartite $d$-regular graphs, to distinguish a set of exactly $\delta N$ vertices of conductance at most $\eta$ from graphs in which every nonempty set of at most $\delta N$ vertices has conductance at least $1-\eta$. This is one fixed threshold, not the Small-Set Expansion hypothesis.
- **Bicliques.** For some fixed $\gamma>0$, Maximum Balanced Biclique and Maximum Edge Biclique are NP-hard to approximate within $N^\gamma$.
- **Dense subgraphs and cuts.** For a fixed $\varepsilon_0>0$, Densest $k$-Subgraph (on fixed-degree bipartite graphs, also with equal quotas on the two sides), Densest At-Least-$k$-Subgraph and Minimum $k$-Cut are NP-hard to approximate within $1+\varepsilon_0$. For Minimum $k$-Cut, a fixed-factor hardness was stated by Saran and Vazirani (1995) without a published proof; the paper gives an explicit derivation.

For most of these problems, every-constant hardness was previously known only under the Small-Set Expansion hypothesis (Raghavendra–Steurer–Tulsiani; Austrin–Pitassi–Wu; Wu–Austrin–Pitassi–Liu; Manurangsi) or under stronger running-time assumptions. The best unconditional factors were 1.00005 for treewidth (Bonnet, 2024) and 1.0003 for treedepth (Bonnet–Neuen–Sokołowski, 2025). The paper's introduction discusses priority problem by problem.

## Repository

```
paper/
  sparsest_cut_consequences.pdf   the paper
  tex/main.tex                    TeX source
```

## Building

The bibliography is inside `main.tex`, so no BibTeX run is needed.

```bash
cd paper/tex
pdflatex main && pdflatex main && pdflatex main
```

## Citation

```bibtex
@misc{zhou2026sparsestcut,
  author       = {Yuwen Zhou},
  title        = {Consequences of constant-factor hardness for uniform sparsest cut: treewidth, bicliques, dense subgraphs and small-set expansion},
  year         = {2026},
  howpublished = {\url{https://github.com/OctopusTide/sparsest-cut-consequences}}
}
```

## License

[CC BY 4.0](LICENSE).
