

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

### Scalable quantum circuit and control for a superconducting surface code

- arXiv:1612.08208v1

A scalable scheme for executing error-correction cycle of a monolithic surface code
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




