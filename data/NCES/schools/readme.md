# Get the data

The NCES school universe file for 2009-2010 is too large to store in the repository, please find it in the [google drive](https://drive.google.com/drive/u/0/folders/1SRrNfgVkxwLKVAThDX_UMu9kwQVvC6aJ)

# School data
NCES currates the Common Core of Data (CCD), which is the authoritative source of data on public schools. 

This directory contains information regarding data for **individual schools**. For current data years, the CCD divides these data into cateogries of *directory* (location), *membership* (enrollment), *staff*, *school characteristics*, and *lunch program eligibility*. Prior to 2014-2015, these categories were collapsed into a single text file. The headers bellow will discuss the data assuming that you are examining a more current data year, but the collapsed file in the earlier years function largely the same. 

This readme describes two data years of interest: **2009-2010** (which was used in Richards, 2014) and **2015-2016** (which is conncurent with the SABINS dataset of attendance zones). The limiting factor in these analyses are the attendance zone datasets, of which at the time of this writing there are really only these two data years which can be used. 

Our analysis utilized the *directory* file to geocode the schools and *membership* files to provide enrollment attributes. 

## Enrollment
Find enrollment data in the membership file, which provides the **count** of students in all US schools broken down by *grade, race, and sex*. These counts can be summed to get the total enrollment in a school, or indexed to examine effects of a policy on specific demographics. 

## Location
Find location (geographic) data on schools in the directory file, which provides latitude and longitude for each school. 

# Matching and indexing
From the documentation:
> Schools are uniquely identified in CCD by the 12-digit variable NCESSCH. This variable is a combination of the state code (the first two digits or FIPST), the Local Education Agency (LEA) ID (the first seven digits or LEAID) and the last five digits (SCHID).

`NCESSCH` should be the primary way that school data are indexed. Telling pandas to read `NCESSCH` as an object (string) is important so that the first two digits (corresponding to state FIPS code) do not get cut off if the first digit is a zero. `NCESSCH` can be useful to index by state and district (LEA) though the later does not have much utility as LEA ID's seem to be largely random outisde of their first two digits, which correspond to a state. That is to say, you cannot search for LEA's in a specific county by indexing the LEA ID to match that of the county FIPS code.

# From the website
>The Common Core of Data (CCD) is the Department of Education's primary database on public elementary and secondary education in the United States. CCD is a comprehensive, annual, national database of all public elementary and secondary schools and school districts.

>Unique NCES ID numbers are assigned to schools and districts when they are initially reported to the U.S. Department of Education by the state education agency (SEA), through EDFacts. Many grant authorizers (Google classroom, Walmart, Target, etc.) require that schools and districts must be listed on the NCES site to award a grant. The NCES ID serves as proof that the entity is listed on the site.

>The NCES school and district locators only provide NCES IDs for public entities.

# Get original data files and codes

navigate to [the Public Schools Universe file webpage](https://nces.ed.gov/ccd/pubschuniv.asp) <br>

link to the [2009-2010 flat codebook webpage](https://nces.ed.gov/ccd/data/txt/psu092alay.txt)

alternatively, find [the pdf for the full 2009-2010 ccd here](https://nces.ed.gov/ccd/pdf/INsc90102a.pdf)
