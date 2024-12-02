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
|    [.github](https://github.com/neccton-algo)         | | [@brajard](https://www.github.com/brajard)        | 4.1          | description of the github organization |
|    [Neccton_Super_Resolution](https://github.com/neccton-algo/Neccton_Super_Resolution)         | | [@AntoineBernigaud](https://www.github.com/AntoineBernigaud)        | 4.4.3       | Super Resolution Data Assimilation |
|    [DINCAE-benthic-traits](https://github.com/neccton-algo/DINCAE-benthic-traits)         | | [@Alexander-Barth](https://www.github.com/Alexander-Barth),[@AbelDechN](https://github.com/AbelDechN)        |   4.2.2 Interpolation          | data products of benthic traits  |
|    [NECCTON_PNMI](https://github.com/neccton-algo/NECCTON_PNMI)         | | [@dlaetitia](https://github.com/dlaetitia)        |   4.3.1          | Spatial distribution of zooplankton diversity in the Parc Naturel Marin Iroise (PNMI) |
|    [BFMFORFABM](https://github.com/inogs/bfmforfabm.git) ||[@plazzari](https://github.com/plazzari) | 5.2.3 and 5.2.4 | POC and bio-optic module used within BFM|
| [plasticparcels](https://github.com/OceanParcels/plasticparcels) | | [@michaeldenes](https://github.com/michaeldenes) | 8.3 | Microplastic transport and dispersion simulation tool based on the `parcels` Lagrangian framework |


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
