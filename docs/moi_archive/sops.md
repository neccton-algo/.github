---
title: SOPs for Software Delivery to Operations
description: Standard Operating Procedures
published: true
date: 2021-02-12T14:48:12.888Z
tags: 
editor: markdown
dateCreated: 2021-01-28T10:23:55.939Z
---

## Introduction
This document proposes a set of Standard Operating Procedures (SOPs) delivering code to Operations.

The main objective is to streamline the deployment of new - or update of existing - operational suites,thus making them more easily maintainable, robust and reliable.

It is a first step towards the streamlining of operations and therefore the satisfaction of all the players:

- **R&D** because they will won't be called upon as often in the event of crashes.
 
- **Services** because it will  improve the quality of service to customers through better product availability.
 
- **QA/Validation** because it will allow to systematically control and measure product quality.

This document is meant to be a living document and as such it is expected to be updated as procedures are fine tuned.

## Release to operations workflow

![release_wf.png](/assets/release_wf.png){.align-center}

### Major steps & responsabilities towards a release

- **R&D** 
	1. open a Change Request ticket in Ops' JIRA
  2. resolve any issues arising during pre-deployment and post-deployment (logged in JIRA)

- **Operations**
	1. pre-deploy (check out, build and tests tag in CI)
  2. deploy (via CI)
  3. post-deployment checks
  4. close JIRA ticket
  
### Patching
If a release candidate require a fix a new release tag will be created containing the fix and the process will restart with the pre-deployment checks.

## Functional Testing and Baseline Data

It is expected that each tagged release will be accompanied by a number of functional tests.
Functional tests are meant to test the outputs of the software against a pre-established baseline.
A baseline is a collection of outputs (well know results)
It's up to R&D to establish what the baseline is and to update the baseline as necessary when code changes significantly. 
Baseline data will be stored in an agreed upon location

## Documentation

When delivering new subsystem components to be integrated into an operational suite (e.g. TEP_BUL, ANA, TEP_SGPS, etc.) it would be ideal to provide documentation in order to allow the ops team to quickly come up to speed with new features and/or significant changes from preavious releases.

The documention can live on a wiki or CMS and be reachable via a URL. This method of documenting software is recommended as it is easy to maintain and update once after the initial effort of creating it.

In general, the information should be arranged in the following categories:

- General information:
	- the name and version of the program. 
	- a brief description of how it works. 
	- the resources used (average data size, computing time etc. ...)
	- the language used for each part (ksh, Fortan, Perl, Python, ...)
	- the machines on which the program has been run.
	- any licenses used (IDL, etc.) and the estimated simultaneous use of these licensess
  - list of exteranal library dependencies
	- any diagrams that may help visualize code complexity, interdependence and sequencing
- Configuration files
	- file type (namelist, environment, etc.)
  - list of important parameters that greatly change the behaviour of the software  
- Inputs
	- upstream dependencies (data sources)
	- list of files needed as input and their location
	- nomenclature of input file names
	- input type (restart, hindcast, previous run, etc.)
	- static files (bathymetry, grid file, etc.)
- Outputs
	- list of output files and their location
 	- naming of the names of these files 
	- location of baseline data for validation
	- temporal coverage of output files
	- downstream dependencies (data consumers)
  - storage requirements (temporary or archival)
- Postprocessing
	- list of post processing tasks and final products

## Progress status reporting
 
All binary programs, (fortran, idl, etc) must create a set of flag files to indicate their progress.
Three states of program execution can be indicated: *start*, *end* or *error*. The flag file name format will be:
 
*PROGRAM_NAME*_R*YYYYMMDD*-[START|OK|ERROR]

*PROGRAM_NAME* must precisely and unambiguously identify the program that created the flag file.
The flag files can be empty except in the case of errors, in which case it must contain an explicit error message.
The destination of the flags needs to be configurable either by parameter passing or within a configuration file.
If the flag nomenclature must contain additional information, it must be inserted between PROGRAM_NAME and RYYYYMMDD and be separated by underscores " _ ".

## Towards a standardised directory layout
The purpose of having a standardized operational environment layout is many fold:

1. Enable as much as possible automated deployment of patches and new software
2. Make it easier to find files when intervention is required
3. Make it easier to run within a scheduling tool specific environment such as EcFlow.
4. Make it easier to clean up and free storage space
5. Make it easier for real time monitoring web services to find data to display


The directory trees below are a generic example...

- For a given suite

├───bin
│    scripts and executables 
├───config
│    configuration files
├───inputs
│		 ln'd or cp'd at beginning of run
│───outputs
│   ├───yyyy
│       ├───MM
│           ├───DD
│		 to be cp'd to centralized storage (archive or other) at end of run
│───products
│   ├───QA
│   │    	qa products
│   └───VA
│ 				plots, etc
│───working
│				  tmp files
│

- For the operational environment

├───bin
│    scripts and executables for all common tasks (post-treatment, QA, plotting, etc
├───config
│    common configuration files
├───inputs
│		  common static inputs
│───suite1
│     ......
│───suite2
│     ......