| [HOME](README.md) |  [Software](Software.md)   |    [Videos](Videos.md)              |
| -------- | ----------------------------------- | ----------------------------------- |



# General instructions

To find out what's available on UB VIDIA via the "%use" magic, just type "use" in the command line (in the Workspace)


Some of the packages are installed as the environments in the anaconda-6.
To find out what's avaialble, do this:

use anaconda-6
source activate base
conda info --env





# Software availability

| Position |                VIDIA                |                Cluster              |
| -------- | ----------------------------------- | ----------------------------------- |
|    1     |                                     |  QMflows                            |



1. QMflows
    cluster:
        module load vidia/quantum-chemistry-py37-Fall2019 
    VIDIA:
        use anaconda-6
        source activate qmflows


2. SHARC
    cluster: 
        N/A
    VIDIA:
        use sharc-2.1.1  (Python 3)

3. DFTB+
    cluster:
        module load dftbplus/19.1-arpack
        module load dftbplus/19.1-dftd3
        module load dftbplus/19.1 
    VIDIA:
        use dftbplus-18.2 (doesn't work)
        use dftbplus-pre-17.1 (works, but less efficient)
        use dftbplus-pre-18.2  (works)

4. CP2K
    cluster:
    VIDIA:
        use anaconda-6
        source activate cp2k-test (just testing)


5. Quantum Espresso
    cluster:
        module load espresso/5.0.2
        module load espresso/5.1.1-static
        module load espresso/5.2.1
        module load espresso/6.1
        module load espresso/6.2.1-epw
        module load espresso/6.2.1
        module load espresso/6.4.1
        module load espresso/6.5
    VIDIA: 
        NA 

6. eQE
    cluster:  
        module load eqe/0.2.0
    VIDIA: 
        N/A

7. NEXMD
    cluster:
        N/A
    VIDIA:
        N/A

8. Psi4
    cluster:
        module load vidia/quantum-chemistry-py37-Fall2019
    VIDIA:
        use libra-4.4.0
        use libra-4.8.1
        use libra-pyscf


9. PyQuante2
    cluster:
        module load vidia/quantum-chemistry-py37-Fall2019
    VIDIA:
        use anaconda-6
        source activate pyquante2  (requires Python 2)


10. HORTON
    cluster:
        module load horton/2.1.1
    VIDIA:
        NA

11. PySCF
    cluster:
        module load vidia/quantum-chemistry-py37-Fall2019
    VIDIA:
        use libra-pyscf
        

12. Newton-X
    cluster: 
        ??
    VIDIA: 
        %use newton-x

13. Open Molcas
    cluster:
        N/A
    VIDIA:
        N/A

14. ErgoSCF
    cluster: 
        module load ergoscf/3.8
        module load ergoscf/3.8-vidia  (with the change)
    VIDIA: 
        ??

15. COLUMBUS
    cluster:
        ?? 
    VIDIA:
        N/A

16. Hefei-NAMD
    cluster:
        module load hefei-namd
    VIDIA:
        N/A

17. Libra
    cluster:
        module load vidia/quantum-chemistry-py37-Fall2019
    VIDIA:
        use libra-4.4.0
        use libra-4.8.1
        use libra-pyscf

18. py3dmol
    cluster:
        module load vidia/quantum-chemistry-py37-Fall2019
    VIDIA:
        use libra-4.4.0
        use libra-4.8.1
        use libra-pyscf


