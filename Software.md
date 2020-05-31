| [HOME](README.md) |  [Software](Software.md)   |    [Videos](Videos.md)              |        [CCR_extra](CCR_extra)       |
| -------- | ----------------------------------- | ----------------------------------- | ----------------------------------- |



# 1. General instructions

To find out what's available on UB VIDIA via the "%use" magic, just type "use" in the command line (in the Workspace)


Some of the packages are installed as the environments in the anaconda-6.
To find out what's avaialble, do this:

use anaconda-6
source activate base
conda info --env





# 2. Software availability & status

|   Software                     |         VIDIA                |         Cluster              |
| ----------                     | ---------------------------- | ---------------------------- |
|  Libra                         | 4.8.1, 4.4.0                 |  4.8.1, 4.4.0                  |
|  Psi4                          |  Yes (version?)              |  Yes (version?)                  |
|  PySCF                         |  Yes (version?)              |  Yes (version?)                  |
|  py3Dmol                       |  Yes (version?)              |  Yes (version?)                  |
|  QMflows-namd                  |           Yes (version?)         |         Yes                  |
|  PyQuante2                     |  Yes (version?)              |  Yes (version?)                  |
|  SHARC                         |           2.1.1                |         No                   |
|  DFTB+                         |   pre-18.2, pre-17.1         |  19.1-arpack, 19.1-dftd3, 19.1     |
|  CP2K                          |  Yes (version?)              |  7.1, 6.1     |
|  ErgoSCF                       |        No                    |  3.8, 3.8-modified    |
|  QuantumEspresso               | No   |  6.5, 6.4.1, 6.2.1, 6.2.1-epw, 6.1, 5.2.1, 5.2.1-static, 5.0.2    |
|  eQE                           | No   |  0.2.0    |
|  HORTON                        | No   |  2.1.1    |
|  COLUMBUS                      | No   | 7.0_2017-12-07 |
|  Newton-X                      | Yes (version?)   |  No |
|  Hefei-NAMD                    | No   |  Yes (version?) |


# 3. To be added:

- OpenMolcas
- NEXMD


# 4. Specific usage notes


* <details>
  <summary>Libra</summary>  
  Description:

  VIDIA:

    Any of the lines

    `use libra-4.4.0`

    `use libra-4.8.1`

    `use libra-pyscf`

  Cluster:

    `module load vidia/quantum-chemistry-py37-Fall2019`

  Notes:

  </details>

* <details>
  <summary>Psi4</summary>  
  Description:

  VIDIA:

    Any of the lines

    `use libra-4.4.0`

    `use libra-4.8.1`

    `use libra-pyscf`

  Cluster:

    `module load vidia/quantum-chemistry-py37-Fall2019`

  Notes:

  </details>

* <details>
  <summary>PySCF</summary>  
  Description:

  VIDIA:

    Any of the lines

    `use libra-pyscf`

  Cluster:

    `module load vidia/quantum-chemistry-py37-Fall2019`

  Notes:

  </details>

* <details>
  <summary>py3Dmol</summary>  
  Description:

  VIDIA:

    Any of the lines

    `use libra-4.4.0`

    `use libra-4.8.1`

    `use libra-pyscf`

  Cluster:

    `module load vidia/quantum-chemistry-py37-Fall2019`

  Notes:

  </details>

* <details>
  <summary>QMflows</summary>  
  Description:

  VIDIA:

    All of the lines

    `use anaconda-6`

    `source activate qmflows`

  Cluster:

    `module load vidia/quantum-chemistry-py37-Fall2019`

  Notes:

  </details>

* <details>
  <summary>PyQuante2</summary>  
  Description: 

  VIDIA:

    All of the lines

    `use anaconda-6`

    `source activate pyquante2`

  Cluster:

    Any of the lines

    `module load vidia/quantum-chemistry-py37-Fall2019`

  Notes: requires Python 2    

  </details>

* <details>
  <summary>SHARC</summary>  
  Description:

  VIDIA:

    Any of the lines

    `use sharc-2.1.1`

  Cluster:

    N/A

  Notes: doesn't include PySHARC

  </details>

* <details>
  <summary>DFTB+</summary>  
  Description:

  VIDIA:

    Any of the lines

    `use dftbplus-pre-18.2`

    `use dftbplus-pre-17.1`

  Cluster:  

    Any of the lines

    `module load dftbplus/19.1-arpack` - a version for TD-DFTB+ calculations, but not parallel

    `module load dftbplus/19.1-dftd3` - a version that includes Grimme's dispersion

    `module load dftbplus/19.1` - a generic version (parallel)

  Notes:   

    `use dftbplus-18.2` - this one is available, but doesn't work due to library conflicts

  </details>

* <details>
  <summary>CP2K</summary>  
  Description:

  VIDIA:

    All of the lines

    `use anaconda-6`

    `source activate cp2k-test` - this is a testing version

  Cluster:

    Any of the lines

    `cp2k/6.1-precompiled`

    `cp2k/7.1-precompiled`

  Notes: 

  </details>

* <details>
  <summary>ErgoSCF</summary>  
  Description: 

  VIDIA:

    N/A

  Cluster:

    Any of the lines

    `module load ergoscf/3.8` - this is the default version

    `module load ergoscf/3.8-vidia` - this is the version with the corrected code needed for NAC calculations!

  Notes: 

  </details>

* <details>
  <summary>Quantum Espresso</summary>  
  Description:

  VIDIA:

    N/A

  Cluster:

    Any of the lines

    `module load espresso/5.0.2`

    `module load espresso/5.1.1-static`

    `module load espresso/5.2.1`

    `module load espresso/6.1`

    `module load espresso/6.2.1-epw`

    `module load espresso/6.2.1`

    `module load espresso/6.4.1`

    `module load espresso/6.5`

  Notes: 

  </details>

* <details>
  <summary>eQE</summary>  
  Description: Embedded Quantum Espresso

  VIDIA:

    N/A

  Cluster:

    Any of the lines

    `module load eqe/0.2.0`

  Notes: 

  </details>

* <details>
  <summary>HORTON</summary>  
  Description: 

  VIDIA:

    N/A

  Cluster:

    Any of the lines

    `module load horton/2.1.1`

  Notes: 

  </details>

* <details>
  <summary>COLUMBUS</summary>  
  Description: 

  VIDIA:

    N/A

  Cluster:

    Any of the lines

    `module columbus/7.0_2017-12-07-bin`

  Notes: 

  </details>

* <details>
  <summary>Newton-X</summary>  
  Description: 

  VIDIA:

    Any of the lines

    `use newton-x`

  Cluster:

    N/A

  Notes: 

  </details>

* <details>
  <summary>Hefei-NAMD</summary>  
  Description: 

  VIDIA:

    N/A

  Cluster:

    Any of the lines

    `module load hefei-namd`

  Notes: 

  </details>


