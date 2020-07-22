| [HOME](README.md) |  [Software](Software.md)   |    [Videos](Videos.md)              |        [CCR_extra](CCR_extra)       |
| -------- | ----------------------------------- | ----------------------------------- | ----------------------------------- |



# 1. General instructions

## Access to the command line

There are three ways to access your own VIDIA container on the command line:

- Run the Workspace tool

- Run the Jupyter Notebooks tool, and open a new noVNC Desktop

- Run the Jupyter Notebooks tool, and run a Terminal 

For the Jupyter Notebooks options, access is provided in the "New" drop-down control.

## `use` in the Workspace

To find out what's available on UB VIDIA via the "%use" magic, start a VIDIA Workspace, then type
"use" on the command line. You'll see a list of the options. "Use"-ing one sets paths and the needed
environment variables to run a given piece of software. Most are specified with the version, such
as `ergoscf-3.8`.

Tip: if you see an error when you enter "use", try this first:

`source /etc/environ.sh`

`use`

### What does `use` do?

To see what really goes on when you invoke use, you can look at the settings created when you run
it. You can list and cat them in the directory: `/apps/share64/debian8/environ.d/`

So when you `cat` the ergoscf-3.8 use script you see that it sets the environment variable `$ERGO`
enabling you to call the executables of ergoSCF.

## conda envs

Some packages are installed as conda envs under anaconda-6. To see a list of available conda envs, issue these commands on the Workspace command line:

`use anaconda-6`

`conda activate`

`conda info --env`

## In Python

To use an environment from Python, 

1. start a Jupyter Notebook or Python session 

1. import the use package from hublib:

    `import hublib.use`

1. then call the "%use" magic to set your paths and your environment:

    `%use anaconda-6`


# 2. Software availability & status

We are now reinstalling all VIDIA packages under the new debian 8 container environment. Current status:

|   Software                     |         VIDIA (version/env)               |         Cluster              |
| ----------                     | ---------------------------- | ---------------------------- |
|  Libra                         | 4.8.1/libra-4.8.1                 |  4.8.1, 4.4.0                  |
|  Psi4                          |                |  Yes (version?)                  |
|  PySCF                         |  1.7.3/pyscf              |  Yes (version?)                  |
|  py3Dmol                       |  0.8.0/libra-4.8.1              |  Yes (version?)                  |
|  pyglet                       |  1.5.7/pyscf              |                    |
|  Nano-QMflows                  |           0.10.1/qmflows         |         Yes                  |
|  QMflows                  |           0.10.1/qmflows         |         Yes                  |
|  PyQuante2                     |                |  Yes (version?)                  |
|  SHARC                         |           2.1.1/pysharc (testing in progress)                |         No                   |
|  DFTB+                         |   19.1         |  19.1-arpack, 19.1-dftd3, 19.1     |
|  CP2K                          |        7.1        |  7.1, 6.1     |
|  ErgoSCF                       |        3.8                    |  3.8, 3.8-modified    |
|  QuantumEspresso               | 6.5 |  6.5, 6.4.1, 6.2.1, 6.2.1-epw, 6.1, 5.2.1, 5.2.1-static, 5.0.2    |
|  eQE                           | 0.2.0   |  0.2.0    |
|  HORTON                        | No   |  2.1.1    |
|  COLUMBUS                      | No   | 7.0_2017-12-07 |
|  Newton-X                      | 2.2-B08 (testing in progress)  |  No |
|  Hefei-NAMD                    | No   |  Yes (version?) |
|  Auto-FOX                    | 0.7.4/qmflows   |  Yes (version?) |
|  CAT                    | 0.9.6/qmflows   |  Yes (version?) |


# 3. To be added:

- OpenMolcas
- NEXMD


# 4. Specific usage notes


* <details>
  <summary>Libra</summary>  
  Description:

  VIDIA:

    `use libra-4.8.1`

  Cluster:

    `module load vidia/quantum-chemistry-py37-Fall2019`

  Notes:

  </details>

* <details>
  <summary>Psi4</summary>  
  Description:

  VIDIA:


  Cluster:

    `module load vidia/quantum-chemistry-py37-Fall2019`

  Notes:

  </details>

* <details>
  <summary>PySCF</summary>  
  Description:

  VIDIA:

    Any of the lines

    `use pyscf`

  Cluster:

    `module load vidia/quantum-chemistry-py37-Fall2019`

  Notes:

  </details>

* <details>
  <summary>py3Dmol</summary>  
  Description:

  VIDIA:

    Any of the lines

    `use libra-4.8.1`

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

    `use dftbplus-19.1`

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

    `use eqe-0.2.0`


  Cluster:

    Any of the lines

    `module load eqe/0.2.0`

  Notes: 

  - basic code for scf, structure optimization, MD (pw)
  - postprocessing programs (pp)
  - CP code: CP MD with ultrasoft pseudopotentials (cp)


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


