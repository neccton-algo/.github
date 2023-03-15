---
title: Good Enough Practices in Scientific Software Development
description: 
published: true
date: 2022-10-14T10:13:14.602Z
tags: 
editor: markdown
dateCreated: 2022-06-29T14:17:40.117Z
---

<div align="center">
<img width="70%" src="/assets/yagni.png" >
  <figcaption><b>You Are Not Going To Need It (YAGNI)</b></figcaption>
</div>

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

</p>
</p>
<div align="center">
<img width="50%" src="/assets/bug_fixing_ways.jpg">
</div>