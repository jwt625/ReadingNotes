

```noteinfo
{
	"date": {
		"y": 23,
		"m": 2,
		"d": 2017
	},
	"tag": [""]
}
```

[back to top](#top)

## 2017 Spring





[toc]


### Scalable ion-photon quantum interface based on integrated diffractive mirrors

[npj quantum information](http://www.nature.com/articles/s41534-017-0006-6)


- microfabricated trap with integrated diffractive mirrors
- couples 4% fluorescence, three times better
- overcomes mode quality limitations of existing integrated optical interconnects

trapped ion:

- coherence time approaching 1min
- qubit gate error rate below $10^{-4}$
- fluorescence:
	1. state readout
	2. create remote entanglement
	- both of which only depend on the fluorescence collection efficiency


Result

- deposite Al on etched substrate
- multi-zone micro-fabricated surface trap with integrated diffractive mirrors













### A scanning transmon qubit for strong coupling circuit quantum electrodynamics

[Nat. Comm.](http://www.nature.com/articles/ncomms2991)


- Scanning transmon qubit. i.e., the transmon fabricated on a $4\times 4 mm^2$ sapphire chip, then glued to a tip of a highlt conductive copper rod on a cryogenic positioning stage, CPW resonators on chip on sample stage. Transmon scanned across the resonator so that coupling vs space can be obtained.


- Spacial distribution of $g$ agrees with simulation.


- A typical movement of the positioning stage of 10um heated the refrigerator from its base temperature of 15mK to over 85mK. Most measurement done between 25 to 35mK


- $T_1, T_2^* \sim 1\mu s$.


- Coulping strength adopted from (this great paper also has a lot information on estimating $T_1$ and $T_2$): `Koch, J. et al. Charge-insensitive qubit design derived from the Cooper pair box. Phys. Rev. A 76, 042319 (2007).`













### Prospective two orders of magnitude enhancement in direct magnetic coupling of a single-atom spin to a circuit resonator


- arXiv:1702.02210v1
- $ g/2\pi = 0.24 $MHz
- spiral geometry (insert figure here)
- $ I_{ac} = \sqrt{( \bar n +1/2 ) \hbar \omega/L_{tot}} $, $ L_{tot} = L_g + L_p $ (geometry inductance + parasite inductance)
- $ L_g \propto N_{loops}^2 \log(N_{loops}) $
- $ g \propto I_{ac} \log(N_{loops}) $
- $L_p$ depends weaker on $ N_{loops} $, hence $g$ increase up to a point where $L_g$ approaches $ L_p$ then $I_{ac}$ begins to drop as $N^\alpha$ with $\alpha < -1$
- dependence of $L_{tot}, J, g/2\pi, Q$ versus $N_{loops}$ from simulation (insert figure)

#### Resulting parameters
- $ g/2\pi = 0.24 $MHz
- $Q \sim 10^4$
- spin initialization $T_{1,init}=2.3\mu s$
- rotation speed $f = 29$MHz, corresponded $ N_{\pi} > 10^5 $



#### Related
- the absence of tunneling states
in a hydrogen-free amorphous silicon film suggesting the
possibility of depositing "perfect" silicon: [Hydrogen-Free Amorphous Silicon with No Tunneling States](http://journals.aps.org/prl/abstract/10.1103/PhysRevLett.113.025503)
- Appendix A of `Koch, J. et al. Charge-insensitive qubit design derived from the Cooper pair box. Phys. Rev. A 76, 042319 (2007)` includes details of network analysis about estimation of capacitances











### Scalable quantum circuit and control for a superconducting surface code


- arXiv:1612.08208v1
- A scalable scheme for executing error-correction cycle of a monolithic surface code
- fast-flux-tunable transmon qubit
- nearest neighbor coupling (flux controlled CZ in this paper)
- eight qubit unit cell realizing quantum hardware and coherent control

#### Intro
- surface code is better than Stean and Shor code concerning hardware requirement
- error rate of qubit gate: single: <0.1%; two-qubit CZ: ~1%
- scalability
	- copy-paste unit cell
	- quantum interconnect between cells in the quantum plane
	- classical control to and from the control plane (already many pursues, see article)
	- crucial to extend the unit cell to control plane to have real scalability (demonstrated in this paper)
	- frequency multiplexing is already heavily exploit in cQED systems, spatial multiplexing is still in its infancy



In this paper:
- flux-controlled CZ gate
- three fixed freq for single-qubit control
- eight detuning sequences for two-qubit gates

#### Background

Surface code QEC
- circuit depth: \# of operations on each ancilla per QEC cycle
- $ \tau_{1Q}=20 $ns, $\tau_{2Q}=40$ns, 500ns for ancilla readout and photon depletion in readout resonator, total 740ns for QEC cycle



Limitations
- fully paralellized X and Z type stabilizer measurements with CZ gate not realized yet
- the CZ gate mentioned above is expected to satisfy:
	- single-qubit gate MW pulse at a fixed small \# of frequencies
	- transmons maximally exploit coherence sweetspot
	- transmons do not cross other interaction zones on their way to/from the intended anti-crossings for the CZ gate
	- flux-pulsing schemes should be scalable with fixed number of detuning sequences and fixed range
	- implementation be compatible with logical qubit operations



First three realized. No fully parallel solution exists with a fixed number
of detuning sequences and a fixed detuning range.

#### The pipelined QEC cycle

#### Questions and unknowns
- Read the surface code paper! (Phys. Rev. A 86, 032324 (2012).)
- microwave-frequency vector switch matrix (VSM)
- Pauli frame updating (PFU)








