![Awesome Fuzzy Logic](assets/hero-banner.svg)
[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![License: MIT](https://img.shields.io/badge/license-MIT-39FF14?style=flat-square&labelColor=0D1117)](LICENSE.md) [![test](https://github.com/aks-builds/awesome-fuzzy-logic/actions/workflows/test.yml/badge.svg?event=push)](https://github.com/aks-builds/awesome-fuzzy-logic/actions/workflows/test.yml)

> A curated, verified list of fuzzy logic theory, libraries, inference tools, and applications — for engineers, researchers, and students working where boolean logic isn't enough.

This list starts at the founding theory (Zadeh, Mamdani, Takagi-Sugeno) and works outward to the software people actually build with: language-specific libraries, dedicated fuzzy inference system (FIS) design tools, neuro-fuzzy hybrids like ANFIS, and real applied projects in control and decision support. Fuzzy logic is a comparatively small, slow-moving field — every entry here was checked against its actual repository, package page, or publisher listing rather than pulled from memory, and each is flagged as either actively maintained or a stable historical reference. This is a starter list (roughly 45 entries at initial publication), not an exhaustive one; see [Contributing](#contributing) if you know of something real that's missing.

**How this is organized, and why it's not another flat A-Z list:**

- **Foundations & Theory** comes first, on purpose — fuzzy logic is built on a small set of specific papers (Zadeh 1965, Mamdani & Assilian 1975, Takagi & Sugeno 1985) that every downstream tool implements one of, so knowing which inference method a tool uses matters more here than in most software categories.
- **Libraries & Toolkits** is grouped by language, not by feature, because a fuzzy logic library's practical value is almost entirely determined by whether it embeds in your existing stack.
- **Fuzzy Inference & Rule Builders** and **Neuro-Fuzzy & Hybrid Systems** are split out from general libraries because they solve a different problem: visually or declaratively *designing* a rule base (FIS builders) versus *learning* one from data (ANFIS and other neuro-fuzzy hybrids).
- **Applications** is deliberately the shortest section. Most real-world fuzzy control ships embedded inside commercial firmware or one-off research code rather than as a maintained standalone open-source project — the few entries here are the ones that are.

### `$ whoami`

Pick a lane — jump straight to the sections that matter for your role.

| Role | Start here |
| --- | --- |
| 🎛️ Control Systems Engineer | [Fuzzy Inference & Rule Builders](#fuzzy-inference--rule-builders) · [Applications](#applications) · [C/C++](#cc) libraries |
| 🔬 ML Researcher | [Foundations & Theory](#foundations--theory) · [Neuro-Fuzzy & Hybrid Systems](#neuro-fuzzy--hybrid-systems) · [Python](#python) libraries |
| 🎓 Student | [Learning Resources](#learning-resources) · [Foundations & Theory](#foundations--theory) |
| 🤖 Robotics Developer | [Applications](#applications) · [C/C++](#cc) libraries · [Fuzzy Inference & Rule Builders](#fuzzy-inference--rule-builders) |

### `$ ls ./sections`

- [Foundations & Theory](#foundations--theory)
- [Libraries & Toolkits](#libraries--toolkits)
  - [Python](#python)
  - [Java/JVM](#javajvm)
  - [C/C++](#cc)
  - [MATLAB/Octave/R](#matlaboctaver)
  - [JavaScript](#javascript)
- [Fuzzy Inference & Rule Builders](#fuzzy-inference--rule-builders)
- [Neuro-Fuzzy & Hybrid Systems](#neuro-fuzzy--hybrid-systems)
- [Applications](#applications)
- [Learning Resources](#learning-resources)
- [Related Awesome Lists](#related-awesome-lists)
- [Contributing](#contributing)
- [License](#license)

## Foundations & Theory

Seminal papers, textbooks, surveys, and standards. Papers and books are judged by continued citation and relevance rather than "maintenance."

- [Driankov, D., Hellendoorn, H., and Reinfrank, M. — An Introduction to Fuzzy Control (2nd ed., Springer)](https://link.springer.com/book/10.1007/978-3-662-03284-8) — A textbook covering the design, stability analysis, and tuning of fuzzy logic controllers.
- [IEC 61131-7:2000 — Programmable Controllers, Part 7: Fuzzy Control Programming](https://webstore.iec.ch/en/publication/4556) — An international standard defining Fuzzy Control Language (FCL) for programming fuzzy control applications on programmable controllers.
- [IEEE Transactions on Fuzzy Systems](https://cis.ieee.org/publications/t-fuzzy-systems) — A peer-reviewed journal published by the IEEE Computational Intelligence Society covering the theory, design, and application of fuzzy systems.
- [Jang, J.-S.R., Sun, C.-T., and Mizutani, E. (1997) Neuro-Fuzzy and Soft Computing](https://archive.org/details/neurofuzzysoftco0000jang) — A textbook combining fuzzy inference systems with neural-network learning methods that introduced the ANFIS architecture.
- [Klir, G.J. and Yuan, B. (1995) Fuzzy Sets and Fuzzy Logic: Theory and Applications](https://books.google.com/books/about/Fuzzy_Sets_and_Fuzzy_Logic.html?id=AOhQAAAAMAAJ) — A graduate-level textbook covering fuzzy set theory, fuzzy logic, and their application to reasoning, control, and decision-making.
- [Mamdani, E.H. and Assilian, S. (1975) "An Experiment in Linguistic Synthesis with a Fuzzy Logic Controller," Int. J. Man-Machine Studies](https://doi.org/10.1016/S0020-7373(75)80002-2) — A paper reporting the first working fuzzy logic controller, built from linguistic rules to control a laboratory steam engine.
- [Mendel, J.M. and John, R.I.B. (2002) "Type-2 Fuzzy Sets Made Simple," IEEE Trans. Fuzzy Systems](https://doi.org/10.1109/91.995115) — A paper formalizing the terminology and computation behind type-2 fuzzy sets, which model uncertainty in membership grades themselves.
- [Ross, T.J. — Fuzzy Logic with Engineering Applications (Wiley)](https://onlinelibrary.wiley.com/doi/book/10.1002/9781119994374) — A textbook covering fuzzy set theory and fuzzy logic applied to control, pattern recognition, and other engineering problems.
- [Takagi, T. and Sugeno, M. (1985) "Fuzzy Identification of Systems and Its Applications to Modeling and Control," IEEE Trans. SMC](https://doi.org/10.1109/TSMC.1985.6313399) — A paper proposing fuzzy models whose rule consequents are linear functions rather than fuzzy sets, defining the Takagi-Sugeno inference method.
- [Zadeh, L.A. (1965) "Fuzzy Sets," Information and Control](https://doi.org/10.1016/S0019-9958(65)90241-X) — The founding paper of fuzzy set theory, defining sets whose membership is graded rather than binary.
- [Zadeh, L.A. (1975) "The Concept of a Linguistic Variable and Its Application to Approximate Reasoning – I," Information Sciences](https://doi.org/10.1016/0020-0255(75)90036-5) — A paper introducing linguistic variables and approximate reasoning as a way to formalize imprecise natural-language concepts.
- [Zimmermann, H.-J. — Fuzzy Set Theory—and Its Applications (4th ed., Springer)](https://link.springer.com/book/10.1007/978-94-010-0646-0) — A textbook covering fuzzy set theory fundamentals and their application in engineering, decision-making, and operations research.

## Libraries & Toolkits

General-purpose programming libraries for building fuzzy sets and fuzzy inference systems, grouped by language.

### Python

- [ex-fuzzy](https://github.com/Fuminides/ex-fuzzy) — A library for building and explaining fuzzy rule-based classifiers using genetic algorithms.
- [fuzzy-c-means](https://github.com/omadson/fuzzy-c-means) — An implementation of the fuzzy c-means clustering algorithm.
- [fylearn](https://github.com/sorend/fylearn) — A scikit-learn-compatible library of fuzzy machine learning algorithms.
- [pyfuzzylite](https://github.com/fuzzylite/pyfuzzylite) — The official Python port of the fuzzylite fuzzy logic control library.
- [PyIT2FLS](https://github.com/Haghrah/PyIT2FLS) — A toolkit for building and simulating interval type-2 fuzzy logic systems.
- [scikit-fuzzy](https://github.com/scikit-fuzzy/scikit-fuzzy) — A SciPy-based library implementing fuzzy sets, fuzzy c-means clustering, and Mamdani-style fuzzy inference.
- [simpful](https://github.com/aresio/simpful) — A library for building and simulating fuzzy inference systems through a readable, high-level syntax.

### Java/JVM

- [fuzzy4j](https://github.com/sorend/fuzzy4j) — A Java library for building fuzzy logic systems.
- [jFuzzyLogic](https://github.com/pcingola/jFuzzyLogic) — A Java library and Eclipse-based editor implementing the IEC 61131-7 Fuzzy Control Language for building and testing fuzzy controllers.

### C/C++

- [eFLL (Embedded Fuzzy Logic Library)](https://github.com/alvesoaj/eFLL) — A C++ library implementing fuzzy logic controllers for embedded systems and microcontrollers such as Arduino.
- [fuzzylite](https://github.com/fuzzylite/fuzzylite) — A C++ library for building fuzzy inference systems, including Mamdani and Takagi-Sugeno controllers.
- [qlibs-cpp](https://github.com/kmilo17pet/qlibs-cpp) — A collection of embedded-systems C++ libraries — signal smoothing, PID control, fixed-point math, and a fuzzy logic inference engine.

### MATLAB/Octave/R

- [frbs (CRAN)](https://cran.r-project.org/package=frbs) — An R package for building and learning fuzzy rule-based systems for classification and regression.
- [fuzzy-logic-toolkit (Octave Forge)](https://octave.sourceforge.io/fuzzy-logic-toolkit/) — An Octave package providing a largely MATLAB-compatible set of functions for building fuzzy inference systems.
- [FuzzyR (CRAN)](https://cran.r-project.org/package=FuzzyR) — An R toolkit, developed at the University of Nottingham, for designing and simulating type-1 and interval type-2 fuzzy logic systems, including a GUI and ANFIS.
- [MATLAB Fuzzy Logic Toolbox](https://www.mathworks.com/products/fuzzy-logic.html) — A commercial MathWorks toolbox for designing, tuning, and simulating type-1 and type-2 Mamdani and Sugeno fuzzy inference systems.
- [sets (CRAN)](https://cran.r-project.org/package=sets) — An R package providing data structures and operations for ordinary and fuzzy sets.

### JavaScript

No actively maintained, dedicated fuzzy-inference (Mamdani/Sugeno) library was found for JavaScript or TypeScript at research time — the candidates checked were either unmaintained since the early 2010s or single-author experiments with no adoption. Note that "fuzzy string matching" packages (e.g. Fuse.js) are a different, unrelated category and are intentionally excluded here.

## Fuzzy Inference & Rule Builders

Tools specifically for building Mamdani or Sugeno fuzzy inference systems visually or via a domain-specific language, as opposed to general-purpose programming libraries.

- [FisPro](https://www.fispro.org/) — An open-source tool from INRAE for designing, learning, and optimizing Mamdani and Sugeno fuzzy inference systems from expert knowledge or numerical data.
- [MATLAB Fuzzy Logic Designer](https://www.mathworks.com/help/fuzzy/fuzzylogicdesigner-app.html) — A MATLAB app, part of Fuzzy Logic Toolbox, for interactively designing, testing, and tuning Mamdani and Sugeno fuzzy inference systems.
- [Xfuzzy](http://www2.imse-cnm.csic.es/Xfuzzy/) — A CAD environment for specifying, verifying, tuning, and synthesizing fuzzy systems to C, Java, or VHDL through its own XFL3 description language.

## Neuro-Fuzzy & Hybrid Systems

ANFIS (Adaptive Neuro-Fuzzy Inference System) implementations and other tooling that learns a fuzzy rule base from data rather than requiring it to be hand-designed.

- [ANFISpy](https://github.com/mZaiam/ANFISpy) — A PyTorch library implementing ANFIS and recurrent variants for regression and classification.
- [evolvingfuzzysystems](https://github.com/kaikerochaalves/evolvingfuzzysystems) — A Python library implementing evolving fuzzy systems that adapt their rule structure online while remaining interpretable.
- [MATLAB — Train ANFIS Systems Using Fuzzy Logic Designer](https://www.mathworks.com/help/fuzzy/train-adaptive-neuro-fuzzy-inference-systems-gui.html) — MathWorks' workflow, built into Fuzzy Logic Designer, for training Sugeno-type adaptive neuro-fuzzy inference systems.
- [twmeggs/anfis](https://github.com/twmeggs/anfis) — A NumPy-based Python implementation of Jang's Adaptive Neuro-Fuzzy Inference System for training Sugeno-type fuzzy systems.

## Applications

Real-world use of fuzzy logic in control systems, decision support, and robotics. This section is intentionally short — see the [C/C++](#cc) and [Python](#python) subsections above for the general-purpose libraries most applied fuzzy control and decision-support projects are actually built on.

- [FCMpy](https://github.com/SamvelMK/FCMpy) — A Python package for constructing and analyzing fuzzy cognitive maps, applied to behavior-change interventions and other decision-support problems.
- [fuzzy_mi_controller](https://github.com/uob-erl/fuzzy_mi_controller) — A ROS package implementing a fuzzy-logic-based variable-autonomy controller for teleoperated mobile robots.
- [pyDecision](https://github.com/Valdecy/pyDecision) — A Python library of multi-criteria decision analysis methods, including fuzzy AHP, fuzzy TOPSIS, and fuzzy VIKOR.

## Learning Resources

Courses, tutorials, and communities.

- [Coursera — Sistemas difusos (Universidad Nacional de Colombia)](https://www.coursera.org/learn/sistemas-difusos) — A university-backed course teaching fuzzy set theory, fuzzy controllers, and rule optimization.
- [FUZZ-IEEE 2026](https://attend.ieee.org/wcci-2026/fuzz-ieee-2026) — The annual IEEE International Conference on Fuzzy Systems, covering current research on the theory and application of fuzzy sets and systems.
- [IEEE Computational Intelligence Society — Fuzzy Systems Technical Committee](https://cis.ieee.org/committees/technical-committees/fuzzy-systems) — The IEEE CIS technical committee coordinating research, awards, and conference activity in fuzzy systems.
- [MathWorks — Fuzzy Logic Toolbox Documentation](https://www.mathworks.com/help/fuzzy/index.html) — Official documentation and tutorials for designing, tuning, and simulating fuzzy inference systems in MATLAB and Simulink.
- [NPTEL — Fuzzy Sets, Logic and Systems & Applications (IIT Kanpur)](https://onlinecourses.nptel.ac.in/noc26_ee38/preview) — A free university course covering fuzzy set theory, fuzzy inference systems, and ANFIS.
- [Stanford Encyclopedia of Philosophy — "Fuzzy Logic"](https://plato.stanford.edu/entries/logic-fuzzy/) — A peer-reviewed encyclopedia entry explaining fuzzy logic as a family of many-valued logics for reasoning under vagueness.

## Related Awesome Lists

- [awesome-artificial-intelligence](https://github.com/owainlewis/awesome-artificial-intelligence) — A curated list of artificial intelligence courses, books, video lectures, and papers.
- [awesome-control-theory](https://github.com/A-make/awesome-control-theory) — A curated list of resources for learning classical and modern control theory.
- [awesome-machine-learning](https://github.com/josephmisiti/awesome-machine-learning) — A curated list of machine learning frameworks, libraries, and software by language.
- [awesome-robotics](https://github.com/kiloreux/awesome-robotics) — A curated list of robotics resources, including libraries, software, and datasets.

## Contributing

Contributions are welcome. Open a pull request that:

1. Adds a project only if it is **OSS-preferred** and either **actively maintained** (commit or release within the last ~24 months — this field moves slower than mainstream ML) or a **stable, widely-cited canonical or historical reference** (papers, textbooks, and standards are judged by continued citation and relevance instead).
2. Places the entry in the most specific existing section or subsection, alphabetized within it.
3. Uses the format: `- [Project name](url) — Short, neutral description ending in a period.`
4. Avoids marketing language, superlatives, or unverified claims.
5. Keeps this a starter list built on depth and verification rather than volume — a genuinely thin subsection is preferable to a padded one.

## License

[![MIT License](https://img.shields.io/badge/license-MIT-39FF14?style=flat-square&labelColor=0D1117)](LICENSE.md)

This work is licensed under the [MIT License](LICENSE.md).
