# Description and guideline on the NECCTON-algo organization
![neccton picture](https://github.com/neccton-algo/.github/blob/main/1500x500.jpeg)
## What is the NECCTON-algo organization?
The NECCTON-algo organization hosts the algorithms developed in the framework of the NECCTON project.

## Guideline for a repository in the organization

### How to add a repository?
Requirements to add a repository to the organization https://github.com/neccton-algo:
- Be a member of the [NECCTON](https://www.neccton.eu/) project
- Put the mandatory files in the respository as described [here](#content-of-a-repository).
- Follow the [recommendations](#recommendations) as much as possible
- Complete the table here :


| Repository name                                       | Branch (default: main) | Owner[^1]                                             | NECCTON task | short description |
|       :---:                                           |  :---: | :---:                                            |     ---:     |    :---            |
| ***Work Package 3***|
| [FABM](https://github.com/fabm-model/fabm) | | [@jornbr](https://github.com/jornbr) | 3.* | Framework for Aquatic Biogeochemical Models (FABM) |
| [ERGOM-NECCTON](https://gitlab.opencode.de/bsh/neccton) | | Anja Lindenthal | 3.2, 5.2.1, 5.2.3 and 5.2.4 | ERGOM-FABM code with DVM and bio-optical modules |
| [BAMHBI for FABM](https://github.com/Ezhen/Bamhbi_submodules) | | [@Ezhen](https://github.com/Ezhen) | 3.2 | FABM implementation of BAMHBI |
| [SEAPODYM-1D-IET](https://github.com/neccton-algo/SEAPODYM-1D-IET) | | [@cls-team](https://github.com/neccton-algo/SEAPODYM-1D-IET/commits?author=cls-team) | 3.2 and 5.2.1 | 1D version of SEAPODYM-LMTL Intermediate Energy Transfert (IET) |
| [PISCES for FABM](https://github.com/MoBelharet/fabm-pisces-4.2) | | [@MoBelharet](https://github.com/MoBelharet) | 3.2 | FABM implementation of PISCES |
| ***Work Package 4***|
|    [.github](https://github.com/neccton-algo)         | | [@brajard](https://www.github.com/brajard)        | 4.1          | description of the github organization |
|    [DINCAE-benthic-traits](https://github.com/neccton-algo/DINCAE-benthic-traits)         | | [@Alexander-Barth](https://www.github.com/Alexander-Barth),[@AbelDechN](https://github.com/AbelDechN)        |   4.2.2 Interpolation          | data products of benthic traits  |
|    [PNMI data paper](https://github.com/neccton-algo/PNMI_data_paper)         | | [@dlaetitia](https://github.com/dlaetitia)        |   4.3.1          | Spatial distribution of zooplankton diversity in the Parc Naturel Marin Iroise (PNMI) |
| [ECOSMO](https://github.com/nansencenter/ECOSMO) | | [@caglartac](https://github.com/caglartac) | 4.3.1 and 5.2.1 | main ECOSMO and diel vertical migration codes |
| [DIIM](https://github.com/carlossoto362/diim) | | [@CarlosSoto](https://github.com/carlossoto362) | 4.4.2 | Python tool for the estimation of marine optical constituents from Remote Sensing Reflectance |
|    [Neccton_Super_Resolution](https://github.com/neccton-algo/Neccton_Super_Resolution)         | | [@AntoineBernigaud](https://www.github.com/AntoineBernigaud)        | 4.4.3       | Super Resolution Data Assimilation |
| ***Work Package 5***|
| [ERSEM-NECCTON](https://github.com/pmlmodelling/ersem-neccton) | [dvm](https://github.com/pmlmodelling/ersem-neccton/tree/dvm) | [@r-millington](https://www.github.com/r-millington) | 5.2.1 | DVM Model in ERSEM |
| [ERSEM-NECCTON](https://github.com/pmlmodelling/ersem-neccton) | [spm](https://github.com/pmlmodelling/ersem-neccton/tree/spm) | [@jimc101](https://www.github.com/jimc101) | 5.2.2 | SPM Model in ERSEM |
| [SPMmodule](https://github.com/giubonino/SPMmodule) | | [@giubonino](https://github.com/giubonino) | 5.2.2 | SPM module |
| [bamhbi-spm](https://github.com/mchoblet/SPM_wave_resuspension) | | [@mchoblet](https://github.com/mchoblet) | 5.2.2 | Bamhbi benthic model (Organic SPM) | 
|    [BFMFORFABM](https://github.com/inogs/bfmforfabm.git) ||[@plazzari](https://github.com/plazzari) | 5.2.3 and 5.2.4 | POC and bio-optic module used within BFM|
| [ERSEM-NECCTON](https://github.com/pmlmodelling/ersem-neccton) | [DOC](https://github.com/pmlmodelling/ersem-neccton/tree/DOC) | [@hpowley](https://www.github.com/hpowley) | 5.2.3 | NECCTON DOC changes in ERSEM |
| [ERSEM-NECCTON](https://github.com/pmlmodelling/ersem-neccton) | [CDOM](https://github.com/pmlmodelling/ersem-neccton/tree/CDOM) | [@hpowley](https://www.github.com/hpowley) | 5.2.4 | CDOM additions for bio-optical model in ERSEM |
| [fabm-spectral](https://github.com/pmlmodelling//fabm-spectral) | [rrs](https://github.com/pmlmodelling/fabm-spectral/tree/rrs) | [@hpowley](https://www.github.com/hpowley) | 5.2.4 | Bio-optical model used with ERSEM|
| [bamhbi-rt](https://github.com/loic-mace/bamhbi-rt) | | [@loic-mace](https://github.com/loic-mace) | 5.2.4 | Bio-optics module for BAMHBI|
| [ECOSMO-MERCY](https://github.com/jbieser/POPCYCLE)) | | [@jbieser](https://github.com/jbieser) | 5.2.5 | Marine POP Cycling module  |
| ***Work Package 6***|
| [Benthic-Habitat-Models](https://github.com/damianobaldan/benthic_habitat_scripts) | | [@damianobaldan](https://github.com/damianobaldan) | 6.2.2 | Benthic habitat mapping markdown  |
| ***Work Package 7&8***|
| [FEISTY](https://github.com/Kenhasteandersen/FEISTY) | | [@KenHasteAndersen](https://github.com/Kenhasteandersen) | 7.3 | Fortran and R implementation of the FEISTY fish community model |
| [OGSTM](https://github.com/inogs/ogstm/tree/neccton_WP8)-[BFM-Hg](https://github.com/BFM-Community/BiogeochemicalFluxModel/tree/neccton_WP8) | neccton_WP8|[@ginRosati](https://github.com/ginRosati)|8.2| Marine biogeochemical mercury model|
| [plasticparcels](https://github.com/OceanParcels/plasticparcels) | | [@michaeldenes](https://github.com/michaeldenes) | 8.2.1 | Microplastic transport and dispersion simulation tool based on the `parcels` Lagrangian framework |
| [Plastic_Poseidon](https://github.com/tamvas3712/Plastic_Poseidon) | | [@tamvas3712](https://github.com/tamvas3712) | 8.2.2 | Marine plastic pollution module  |
| [MEDSLIK_II_NECCTON](https://github.com/Sliubartseva/MEDSLIK_II_NECCTON) | | [@SLiubartseva](https://github.com/Sliubartseva/MEDSLIK_II_NECCTON/commits?author=Sliubartseva) | 8.2.3 | MEDSLIK-II code for NECCTON project |
| [CanMETOP](https://zenodo.org/records/11214066) | | [Zhiyong Xie](https://www.hereon.de/institutes/coastal_environmental_chemistry/organic_environmental_chemistry/team/098611/index.php.de) | 8.2.5 | POPs’ Global atmospheric transport model |
| [ECOSMO-MERCY](https://github.com/jbieser/HAMSOM-ECOSMO-MERCY) | | [@jbieser](https://github.com/jbieser) | 8.2.5 | Marine Mercury Cycling and Bioaccumulation module |
| [Bfiat](https://github.com/EMODnet/Bfiat) | | [@karlines](https://github.com/karlines) | 8.2.6 | Bottom Fishing Impact Assessment Tools  |
| [CC Indices](https://github.com/pmlmodelling/neccton_cc_indices) | | [@ledm](https://github.com/ledm) | 8.4 | Climate Change Stressor Indices |

[^1]:indicate here the github login of the main contact for the code.

### Content of a repository
A GitHub repository of the NECCTON GitHub organization contains the following file:

- A `LICENCE` file: NECCTON encourages the use of open-source licences.
- A `CODEOWNERS`file: indicate the main contacts for the repository. See [here](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners) for more details.
- A `README` file: see the minimum requirement for the README file [here](#readme)
- One or several Jupyter notebooks to demonstrate the algorithm and the baseline. The baseline corresponds to an existing algorithm or a minimal solution (e.g. linear regression) that the algorithm is expected to outperform. 

#### README
The README file must contain a description for:
- the data source
- the baseline (or a link to the jupyter notebook of the baseline)
- the metrics used to validate the output(s) of the algorithm
- the list of dependencies (name of the dependency and full version number used) needed to use the code, and use language-specific tools to install the dependencies (recommended)
- the documentation (e.g., via a link). It should allow a potential user to understand the code and reuse it. The documentation will be available at the M36 of the NECCTON project.
- Citations and links for NECCTON publications using or introducing the code, when applicable.

### Recommendations
In addition to the points mentionned above, it is strongly suggested to:
- Use a data API for easy access to the data when testing the code
- Make use of GitHub actions to run unit tests when pushing the code on the repository (or when merging with the `main` branch). See [here](https://docs.github.com/en/actions) for a documentation of GitHub actions.
- Use language specific tools (e.g. conda, pipenv) to define the running environment.
- Use the latest best coding practices. For more details, see [here](https://github.com/neccton-algo/.github/blob/main/docs/moi_archive/best_practices.md)
- Upload code to the organization code that is specific to the NECCTON project. Other generic tools can be hosted elsewhere.

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
