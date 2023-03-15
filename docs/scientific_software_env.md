---
title: The scientific development/operational environment
description: Some diagrams...
published: true
date: 2021-05-11T14:00:41.390Z
tags: 
editor: markdown
dateCreated: 2021-05-11T14:00:41.390Z
---

# What we would like to achieve

## Ideal environment
![environmanent.png](/assets/environmanent.png){.align-center}
[Edit me!](/assets/environment.drawio) (produced with https://app.diagrams.net/)

## Ideal release-to-operations workflow
![release_wf.png](/assets/release_wf.png){.align-center}
[Edit me!](/assets/release_wf.drawio)

## How do we get there

Just a brain dump... some goals maybe more achievables than others

### Software development
- General
	- Coding standards
  -	Standardised project layouts
  - Code analysis is great but only if steps are taken to improve scores. When possible 
  - Set up inhouse [python library repo](/personal/gturek/pypi_repo) to encourage code reusability
    
- Version control
  - Encourage and support migration from SVN to GIT as much as possible
  - A simple ticketing system for SVN holdouts?
  - Encourage best practices:
  	- [gitlab workflow](/tools/GitLabWorkflow)
    - Precommit hooks to ensure ticket <-> commit
    - Locked main/production branches/tags
    
- Testing
	- Unit and/or functional testing
	- Jenkins and GitLab-CI training for R&D?
	- Use docker for testing complex environments
  
### Deployment

- Automate as much as possible
- Pre-operational testing
  
### Operations

- Publish official [MO Operators manual](https://sulu.mercator-ocean.fr/moi-oper-manual/). This includes cleaning up what is duplicated in this wiki
- JIRA ticketing for all ops tasking and incindent reporting
- Move away from cron to EcFlow (further investigate [Cylc](https://www.cylc.io)?)
- Replace SUP with a web interface
- Library of useful scripts (refactor & generalise)?
- Can we assist with model modularisation?

  
        
