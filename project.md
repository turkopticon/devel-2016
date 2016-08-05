# Turkopticon 2.0

This document establishes the scope of the current major development period of the Turkopticon service and web app.

## Core team

||||
---- | ---- | ----
Six Silberman | Lilly Irani | Kai Li

## Table of contents
<!-- TOC anchor -->

- [Turkopticon 2.0](#turkopticon-2.0)
- [Core team](#core-team)
- [Table of contents](#table-of-contents)
- [Justification](#justification)
- [Scope](#scope)
- [Objectives](#objectives)
- [Exclusions](#exclusions)
  - [Moderation](#moderation)
- [Deprecation](#deprecation)
- [Timeline](#timeline)

## Justification

Noticeable unrest and dissatisfaction stems from the current inherently subjective rating system. To provide a better user experience, this project will move Turkopticon toward a HIT-based, objectively oriented rating system.

## Scope

This project alters the core data architecture of Turkopticon to accept an objectively oriented rating of HIT attributes instead of subjectively oriented requester attributes, and aims to achieve the following: 

- Promote consistent and reliable user-driven data.
- Allow the review of HITs.
- Mitigate and prevent future conflict based on an open-ended design.
- Provide both recent (past 90 days) and lifetime statistics.

The project will be complete by `TBD`.

## Objectives

- Database
  - create new tables with fields mapped to review form inputs
- Review form
  - provide conditional expansion for semantic validation
  - define fields that provide clear, useful, and objective data
  - write to new database structure
- Site interface and layout 
  - update the display of data via review partials
  - revamp header
  - remove footer
- API
  - move toward accepted best practices for REST APIs
  - serialize new collections reflecting new data architecture
- Userscript and browser extension
  - rewrite for new API and return data
  - design and integrate a simple, informative display based on return data
- Test suite
  - create collection of test cases for the codebase
  
## Exclusions

### Moderation

This project does not expect resolution to the general dissatisfaction or "toxicity" apparent in the community. Re-evaluation of current moderation practices may need to be reviewed at a later date to address the remaining issues.

## Deprecation

Since this project massively changes the core data architecture, future and past data will be mutually incompatible. This project will not introduce or attempt to provide any conversion algorithms.

Past data will remain available for `TBD` months to help ease the transition into the new format and provide canonical data if necessary. 

## Timeline

`TBD`