# Description and guideline on the NECCTON-algo organization
![neccton picture](https://github.com/neccton-algo/.github/blob/main/1500x500.jpeg)
## What is the NECCTON-algo organization

## Guideline for a repository in the organization

### How to add a repository?
Requirements to add a repository to the organization https://github.com/neccton-algo:
- Be a member of the [NECCTON](https://www.neccton.eu/) project
- Put the mandatory files in the respository as described [here](#content-of-a-repository).
- Follow the [recommendations](#recommendations) as much as possible
- complete the table here :

| Repository name                                       | Owner[^1]                                             | NECCTON task | short description |
|       :---:                                           |  :---:                                            |     ---:     |    :---            |
|    [.github](https://github.com/neccton-algo)         | [@brajard](https://www.github.com/brajard)        | 4.1          | description of the github organization |


[^1]:indicate here the github login of the main contact for the code.

### Content of a repository
A github repository contains the following file:
- A `LICENCE` file: NECCTON encourages the use of open source codes.
- A `CODEOWNERS`file: indicate the main contacts for the repository. See [here](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners) for more details.
- A `README` file: see the minimum requirement for the README file [here](#readme)
- One or several jupyter notebook to demonstrate the algorithm and the baseline.

#### README
The README file must contain a description for :
- the data source
- the baseline (or a link to the jupyter notebook of the baseline)
- the metrics used to validate the output(s) of the algorithm
- the dependencies needed to use the code, or use language specific tools (recommended)

### Recommendations
In addition to the points mentionned above, it is strongly suggested to:
- Having a data API to have a easy access to the data when testing the code
- Make use of GitHub actions to run unit tests when pushing the code on the repository (or when merging with the `master` branch). See [here](https://docs.github.com/en/actions) for a documentation of GitHub actions.
- Use language specific tools (e.g. conda, pipenv) to define the running environment.
- Use the latest best coding practices.

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
