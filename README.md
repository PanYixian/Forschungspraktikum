# Forschungspraktikum
codes for Forschungspraktikum

Project_description:

    task1: same geometry, but different atomic ordering
    task2: same geometry, but different order and require global rotation/translation
    task3: 2 MD-snapshots of the same molecule, i.e. slightly different geometry + different order
    task4: parts of the molecule really different
    task5: addition if there is time, H replaced by CH3 or similar


Record of paper-reading

paper1:
MOLFIT: A computer program for molecular superposition (P.K.Redington, Computers & Chemistry, Volume 16, Issue 3, 1992, 217-222)
- direct noniterative method for determining the unitary matrix which superimposes one structure upon the other
- refine by improved SS algorithm (1991, Sippl & Stegbuchner)
- !!! place the molecule centers at the origin (0,0,0)
- superposition of two atoms: rotate the vector of one atom parallel to the other
- Nyburg's algorithm: three subproblems of least-squares (x,y,z) (how is it iterated?)
- SS algorithm: use first and second derivatives to determine minimum (possible problem of convergence)
- BFGS algorithm: Euler rotation matrix
- !!! initialization: align the first three vectors(atoms)? may save some later calculations?

paper2:
Computational methods for the structural alignment of molecules (C. Lemmen & T. Lengauer, Journal of Computer-Aided Molecular Design, 14: 215–232, 2000.)
- matching-based: Boltzmann-machine
- optimization-based: simplex optimization of the molecular electrostatic fields, Hodgkin similarity index
- grid-based: electron density overlap optimization using Fourier space methods, electron den- sity approximated by sets of Gaussian functions
- graph-based: clique detection, distance compatibility graph
