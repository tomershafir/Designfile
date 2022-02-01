# Designfile

## Intent

Designfile method suggests to write system architecture, high-level or detailed design documents (when appropriate) and store them as part of the project files, using [IEEE-1016-2009-SDD's](https://ieeexplore.ieee.org/document/5167255) description of content and organization, entirely or partially.

## Motivation

[SDLC](https://www.guru99.com/software-development-life-cycle-tutorial.html) is a systematic process for building software. Generally SDLC includes:

- Requirement collection and analysis
- Design
- Coding
- Testing
- Deployment
- Maintenance

There are all kind of [models](https://www.javatpoint.com/software-engineering-sdlc-models) that suggests how to sdlc.

Design phases are crucial in SDLC and highly affects a lot of important aspects in projects, and there are generally several levels of design. In some projects, it is appropriate to document the design, depending on several aspects, including:

- The problems' complexity
- The solutions' complexity
- The project's size
- Applied methodologies, e.g. prototyping approach may not go hand by hand with design documentation
- Cross-cutting concerns documentation needs
- Org documentation needs

Generally, design documents are digital documents that contain implementation strategy and key design decisions with emphasis on the trade-offs that were considered during those decisions. It should be informative, precise and concise at the same time. The ultimate goal of a design document is to facilitate communication and alignment.

## Designfile.md

- Use "Designfile" name for design files, in analogy to existing naming conventions.
- Use Markdown for Designfiles as it fits-in well, because it allows to write easy-to-read and easy-to-write plain-text platform-independent content using a rich set of features and possibly convert it to HTML or XHTML with ease. Refer to [The Markdown Guide](https://www.markdownguide.org) for more info.

## Modularity

Dependending on the problems' complexity, the solutions' complexity and the project's size, a single Designfile conatining all the documentation may be cluttery.

To overcome this, I suggest to distribute the design documentation accross several Designfiles by seperating concerns. This can improve modularity, readability and elegance of the Designfiles. You can have a Designfile per directory or module if it is appropriate. Don't store more a single Designfile per directory.

Designfiles should contain references(e.g. URIs) to related Designfiles according to their hierarchy to explicitly express dependencies. For example, top-level design file will contain references to all secind-level Designfiles.

## Desing Levels

Designfiles may be used for all levels of design: architecture, high-level design or detailed design. The modularity of Designfiles allows to easily arrange documentation of all levels of design.  

## Content and Organization

You should include content and organize it in Designfiles according to the [IEEE-1016-2009-SDD](https://ieeexplore.ieee.org/document/5167255) standard.

### Example Template

- Frontspiece
  - Date of issue and status
  - Issuing organization
  - Authorship
  - Change history
- Introduction
  - Purpose
  - Scope
  - Context
  - Summary
- References
- Glossary
- Body
  - Identified stakeholders and design concerns
  - Design viewpoint 1
  - Design view 1

   …

  - Design viewpoint n
  - Design view n
  - Design rationale

## Lifecycle

1. Creation and rapid iteration
2. Review and iteration
3. Implementation and iteration
4. Maintenance and learning

## Designfile Pros

- Improved Understandability: design doc is the most accessible entry point to learn about the thinking that guided the creation of the system
- Improved Maintainavility
- Improved Findability of Components
- Encourages Reusability
- Improved Accessibility: Designfiles are stored as part of the project, so SWEs can easily access and read from or write to them
- Version Control and Collaboration: Designfiles are stored as part of the project, so they can be checked into the used SCM to achieve version control and collaboration
- Degree of Standarization
- Saves Money: upfront investigation and resolution of problems and pitfalls

## Designfile Cons

- Time and Budget: it takes time to write good Designfiles, and thus it requires budget too
- Writing Is Hard
- Components Management and Maintenance Overhead: you now need to manage and maintain additional components - the Designfiles
- Storage Overhead
- Open Source: security may be compromised, because hackers can more easily detect vulnerabilities by reading Designfiles. If Designfiles are not checked into the SCM in an open-source project, then there is no version control and collaboration is difficult
- Clutter
- Embracement of Non Proficients: people who can't understand the code without additional documentation are probably not technically proficient for the job, and the design documentation allows such people to collaborate and possibly damage the project

## Why not document design in README?

A [README](https://en.wikipedia.org/wiki/README) file contains information about the other files in a directory or archive of computer software. A README file typically encompasses configuration instructions, installation instructions, operating instructions, a file manifest, copyright and licensing information, contact information, troubleshooting instructions, credits and acknowledgments and more. Why not:

- Messy: inclusion of design inside READMEs, together with all the other things READMEs contain, may result in messy files and damage the first impression about projects.
- Different Purpose: READMEs are very general and have many purposes, while design documentation is generally not one of them.
- Tight Coupling: design doc is tightly coupled with README files and it makes it harder to independently distribute desing doc when necessary.

## Why not document design in source files?

Source files contains the code that defines the application. Documentation in source files usually appears in the form of a comment. Why not:

- Messy: documnetation in source files should be short(but informative) to keep the source files readable and clean. Inclusion of design may result in messy source files.
- Different Purpose: the purpose of documentation in source files is to express functionalities of sofware components or to mention key notes, differently from the purpose of design docs.
- Encapsulation: inclusion of design documentation in source file may expose implementation details and break encapsulation at some level.

## References

- [https://www.markdownguide.org/](https://www.markdownguide.org/)
- [https://people.eecs.berkeley.edu/~kubitron/courses/cs162-F07/design.html](https://people.eecs.berkeley.edu/~kubitron/courses/cs162-F07/design.html)
- [https://www.industrialempathy.com/posts/design-docs-at-google/](https://www.industrialempathy.com/posts/design-docs-at-google/)
- [https://blog.bit.ai/software-design-document/](https://blog.bit.ai/software-design-document/)
- [https://www.range.co/blog/better-tech-specs](https://www.range.co/blog/better-tech-specs)
- [http://cengproject.cankaya.edu.tr/wp-content/uploads/sites/10/2017/12/SDD-ieee-1016-2009.pdf](http://cengproject.cankaya.edu.tr/wp-content/uploads/sites/10/2017/12/SDD-ieee-1016-2009.pdf)
- [https://en.wikipedia.org/wiki/Software_design_description#cite_note-4](https://en.wikipedia.org/wiki/Software_design_description#cite_note-4)
- [https://en.wikipedia.org/wiki/README](https://en.wikipedia.org/wiki/README)
- [https://www.oreilly.com/library/view/c-cookbook/0596007612/ch01s19.html](https://www.oreilly.com/library/view/c-cookbook/0596007612/ch01s19.html)
- [https://ieeexplore.ieee.org/document/5167255](https://ieeexplore.ieee.org/document/5167255)
- [https://www.gnu.org/software/make/manual/make.html](https://www.gnu.org/software/make/manual/make.html)
