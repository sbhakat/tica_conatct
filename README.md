# Local fluctuations promotes water access to protein
The core of a protein is held together by hydrogen bond interactions involving backbone amides. Local fluctuations or complete unfolding of a protein breaks the hydrogen bonds involving backbone amides (NH) and allows water penetration. This allows hydrogen exchange (HX) between NH and the hydrogen atoms of the solvent water molecules. Thus, the HX rates, which can be measured by NMR spectroscopy or mass spectrometry, can give valuable information about the local stability of the protein structure as well as conformational changes and folding pathways.

BPTI is like a rock. The local fluctuation in the loop region opens up the cavity which enables HDX between Ile18NH and water. However, this is a very slow process. In millisecond long MD simulation of DESRES (within M1 ensemble) the loop fluctuation has very few sampling. In this project I have used TIC to capture the slow degrees of freedom associated with this loop motion. The TIC combined with PT-Metad-WTE enables better sampling of the conformational space.

Our proposed HDX mechanism

![bpti-hdx](/hdx-mechanism.png)

The following Figure shows the Loop region in BPTI. Local fluctuations in the loop motion breaks the H-bond interactions which allows solvent penetration.

![bpti](/local-fluctuation.png)

The following Figure shows what I meant by FW and SW in the Jupyter Notebooks

![bpti-water](/water-bpti-fwsw.png)

The following Figure shows the so called 'spectral gap' along a RC (TICs). Keep an eye on the timescale (in this case frames) seperation.

![tic-seperation](/left-righttic.png)

Timescale of the process (Zero indexed)

![tica-timescale](/timescale-sgoop-new.png)

The above figure is comparable to Figure 14D in Ghosh et al. 'The maximum caliber variational principle for nonequilibria', Annual Review of Physical Chemistry, 16:2, 2020 (link: https://www.annualreviews.org/doi/10.1146/annurev-physchem-071119-040206). This generalizes TICA and SGOOP. The exact mathematical similarity will be proven in upcoming paper.

Sampling of the solvated state (DESRES vs Metadynamics): using TIC CV combined with PT-Metad-WTE

![metaddesres-timescale](/desres-metad.png)

Notes:

1. See Analysis folder to see how I generated the TICA.

2. See Table S2 in the paper entitled 'Transient access to the protein interior: Simulation vs NMR' by Persson and Halle to see the definition of M1 state.

3. See 'How amide hydrogens exchage in native proteins' to see how one can calculate HDX from molecular simulation using simple cutoff distance.

4. Check the attached Figure to see what I meant by loop motion.

It is important to mention SGOOP and TICA are both mathematically connected by Principle of maximum entropy. For details regarding TICA and its connection with maximum entropy one should check the following paper:

Bell AJ, Sejnowski TJ (November 1995). "An information-maximization approach to blind separation and blind deconvolution". Neural Comput. 7(6): 1129–59. CiteSeerX 10.1.1.36.6605. doi:10.1162/neco.1995.7.6.1129
