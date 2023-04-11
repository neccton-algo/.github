# Best practices
The document is adpated from a [Mercator](https://www.mercator-ocean.eu/en/) document (thanks Renaud)

## Coding

- Follow the [KISS](https://en.wikipedia.org/wiki/KISS_principle) principle
- Follow the [YAGNI](https://en.wikipedia.org/wiki/You_aren't_gonna_need_it) principle
- Follow the [FAIR Principles for Research Software](/public/software/fair)
- Do not be afraid to refactor
- Make dependencies and requirements explicit
- Avoid code duplication: decompose programs into functions/methods
- Use well known (and therefore tested) code libraries
- Flags, paths, options in configuration files
- Remove unused code rather than comment
- Optimize only after software runs correctly
- Use language specific code styling conventions (variable naming, indentation, etc, etc)
	- self-explanatoring naming for variables and functions/methods names
- Test, test, test
	- unit tests (function/methods)
  - functional/verification tests with established baselines
 - Consider generalising for code reuse and sharing
 - Consider modularization
  
  ## Tools
  
- Comment/document
	- pick an automatic documentation generator and learn how to annotate the code so that the doco can be generated for you.
 - Track your work with issue tracking software
- Use version control
	- adopt a basic repository strategy (master/branches/tags)
	- commit often for incremental changes
	- merge requests and code reviews
- Make use of CI/CD Continuous Integration & Continuous Deployment
	- run tests at each commit
- Use build frameworks when necessary (cmake)
- Use packaging when available (conda, pip)
- Use Quality Analysis tools (linters, test coverage, static code analysis) to identify duplication, vulnerability, potential bugs, etc

