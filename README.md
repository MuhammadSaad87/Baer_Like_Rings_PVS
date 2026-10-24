Formalization of Baer-Like Rings in PVS
A PVS formalization of Baer, Rickart, quasi-Baer and principally quasi-Baer (p.q.-Baer) rings. It is built on the algebra library of NASALib, the NASA PVS Library.
The development accompanies the paper Formalization of Baer-Like Rings in PVS by Muhammad Saad, Majed Zailaee and Ahmed Saleh.
Contents
Theory	Content
`idempotent_def`	Idempotent elements of a groupoid
`special_subrings`	Left and right annihilators and their Galois connection, unital subrings, the center as a ring, corners eRe
`ring_with_one_principal_ideal_def`	One-sided principal ideals aR and Ra, the two-sided principal ideal, and their annihilators
`nilpotent_def`	Nilpotent elements and reduced rings
`special_rings_with_one`	Semicentral and central idempotents; Abelian, semicentral reduced, Boolean and prime rings
`baer_ring_def`	Baer, Rickart, quasi-Baer and p.q.-Baer rings and their basic relations
`baer_ring_lemmas`	Abelian/reduced characterizations, corners, the center, prime rings
`baer_instance_int`	Consistency check: instantiation of the development with the integers
Import order:
```
idempotent_def
  -> special_subrings
       -> ring_with_one_principal_ideal_def
       -> nilpotent_def
            -> special_rings_with_one
                 -> baer_ring_def
                      -> baer_ring_lemmas
                           -> baer_instance_int
```
Main results
Kaplansky's left-right symmetry of the Baer condition (`baer_equiv`).
Clark's four equivalent forms of the quasi-Baer condition (`quasi_baer_equiv`).
A ring is Abelian Baer iff it is reduced quasi-Baer (`baer_quasi_baer`).
A ring is Abelian (right, left) Rickart iff it is reduced (right, left) p.q.-Baer (`rickart_pq_baer_right`, `rickart_pq_baer_left`, `rickart_pq_baer`).
The Baer, right Rickart, left Rickart, Rickart and quasi-Baer properties pass between a ring and all of its corners eRe (`baer_corners`, `right_rickart_corners`, `left_rickart_corners`, `rickart_corners`, `quasi_baer_corners`).
The center of a quasi-Baer ring is a Baer ring (`quasi_baer_center`).
A ring with identity is prime iff 1 ≠ 0 and aRb = 0 implies a = 0 or b = 0 (`prime_ring_iff`).
A ring with identity is prime iff it is quasi-Baer (equivalently right p.q.-Baer, left p.q.-Baer, or p.q.-Baer) and semicentral reduced (`prime_and_quasi_baer`).
Verification status
Item	Status
Formulas, judgements and TCCs	130 in total; 128 proved
`rickart_center`, `pq_baer_center`	Stated as `CONJECTURE`s from the literature; not proved
Dependencies	No proved result depends on the two conjectures
The complete output of the batch run is in `verification-log.txt`.
Requirements
PVS 7.1 (tested with 7.1.0): https://pvs.csl.sri.com/
NASALib v7.1.1: https://github.com/nasa/pvslib. Its root directory must be on `PVS_LIBRARY_PATH`. The theories import it as `algebra@...`.
Reproducing the results
Install PVS and NASALib, and add the NASALib root directory to `PVS_LIBRARY_PATH`.
Clone this repository and start PVS in its directory.
Open `baer_instance_int.pvs` and run `M-x prove-importchain`, then `M-x status-proof-importchain`.
The expected result is 130 formulas: 128 proved, and 2 untried conjectures.
Citation
If you use this development, please cite the accompanying paper:
> M. Saad and A. Saleh. *Formalization of Baer-Like Rings in PVS*. (Submitted.)
Contact
Muhammad Saad, m.saad@alexu.edu.eg
