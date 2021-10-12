# Geosnap4ed: educational inequality through a spatial lens

The geosnap4ed project is designed increase field understanding of how to use spatial extents and
the neighborhood dynamics therein as inputs toward identifying how best to support schools serving
Black, Latino, and low-income students

## Overview

This repository serves as a central vehicle for communication between team members. It is used to :

1. store shared data (or links thereto) for understanding their properties and idiosyncrasies before using them in analyses or incorporating into the geosnap database
2. raise questions and provide feedback for the @spatialucr team by using [issues](https://github.com/spatialucr/geosnap4ed/issues)
3. document progress toward the project's goals
4. share and centralize notes (and links) to planning, testing, and research documents

Note that much of the project's labor will be reflected in the
[geosnap](https://github.com/spatialucr/geosnap), [tobler](https://github.com/pysal/tobler),
[segregation](https://github.com/pysal/segregation), and workshop (e.g.
[NARSC](https://github.com/sjsrey/pysalgeosnapnarsc21)) repositories rather than in *this*
repository. Instead, the files here should be treated as intermediate/temporary storage, and the
notebooks as beta-tests for internal collaboration and discussion, prior to making them public.

## Background

This project will build on [`geosnap`](https://github.com/spatialucr/geosnap)'s neighborhood
construction capabilities to include additional educational data parameters in neighborhood
construction, its data processing pipeline, its analytical capacity, and its ease of use for the
foundation and the field (large national nonprofits, policymakers, researchers). Enhancement to the
package will proceed in two primary phases.

During the first phase, the team will integrate new data sources and methods into the software
package. During the second phase, the team will develop training materials, engage with external
stakeholders, and conduct outreach through academic conferences and targeted demonstrations. The
investment will thus facilitate several extensions to the existing software and analytical landscape
including:

1. Building additional interfaces to educational data sources (including Stanford Education Data
   Archive and the Urban Institute’s Education Data API) and new analytical methods into the
   standard set of geosnap tools. As with existing datasets, these will be hosted and available
   through the spatialucr [quilt data server](https://open.quiltdata.com/b/spatial-ucr), which eases
   the process of procuring data for further analysis.
2. Making new segregation analytics available through the geosnap package. This will facilitate the
   analysis of different racial and economic segregation patterns at multiple scales and will allow
   analyses of whether segregation patterns are statistically improving.
3. Developing and integrating a novel suite of location-allocation models for understanding
   trade-offs in the siting of critical resources. These models can be used, e.g. for determining
   the optimal placement for a new after-school mentoring service that requires minimal commuting
   for needy students.
4. Developing and integrating new techniques for modeling data transformations between geographic
   units. Standardizing spatial units of analysis for different educational and neighborhood data is
   among the most challenging tasks in current work. The grant will support enhancements to the
   PySAL `tobler` package, which is tightly integrated into geosnap.
5. A series of community engagement activities designed to 
   1. incorporate feedback on the component design, progress, and extensions; 
   2. train and mentor a diverse group of young scholars and policy professionals; and 
   3. disseminate educational materials to community stakeholders through computational notebooks.
      Community feedback on both implementation and training materials are incorporated continuously
      throughout the life of the grant through both synchronous (i.e. digital workshops, community
      code sprints, and case study presentations) and asynchronous (i.e. issues closed, forks
      created, contributions merged) feedback mechanisms. These allow the developers to both
      maintain a transparent relationship with a broad user-base as well as implement specific
      features and enhancements tailored to the educational community.

## Organization

The repository is currently organized into four subdirectories:

- `data`: datasets, links to datasets, or placeholders for workflows carried out in the notebooks
- `notebooks`: jupyter notebooks for collaboration or discussion
- `notes`: docs and links to project botes
- `tools`: scripts for automating processes and generating admin content

## [Project planning notes](https://hackmd.io/CVR4gbd8TsW872VG23OxEA)
