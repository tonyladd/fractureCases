Sample cases for fractureFoam

frac: Test of 2D aperture model with transport corrected linear kinetics
    (Models/reacLin.H)
    Screenshots of fields (H, C0, Ux, Uy)
    Note: 2nd order upwind scheme can lead to small negative concentrations
    (C60.png and C80.png)
    In this test G = 1 and h_inlet(t) = 2sqrt(1+t)-1 
    This test takes about 10 mins on a single core 

seed: Test of 2D aperture model with a seeded fracture
    (Models/reacLin.H)
    This test takes about 15 mins using 4 cores
    Screenshots of concentration field + line plots of C(0,z) & C(W/2,z)
    
    results/NL: Test of nonlinear kinetics with a seeded fracture
    (Models/reacNonlin.H)
    This test takes about 2.5 hours using 4 cores; the extra cpu time is
    for iterating the concentration field
    Screenshots of concentration field + line plots of C(0,z) & C(W/2,z)
    are in seed/results/NL
    Note slow decay of C in initial fracture (non-linear kinetics)
         
calciteNL: Test of non-linear kinetics in a random fracture
    (Models/reacNonlin.H)
    This test takes about 1.5 hours using 4 cores
    Screenshots of concentration field
         
Version:
Source code is in fractureFoam (v1 + OpenFOAM-4.x)
Note: Advection is now 2nd order (linearUpwind in fvSchemes)
