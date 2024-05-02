# Bioinformatics pipeline for "Idiosyncratic responses to biotic and environmental filters in wood-inhabiting fungal communities"

This pipeline is a pre-release version of the OptimOTU pipeline, which is
implemented in R using the [{targets}](https://books.ropensci.org/targets/)
pipeline tool.
It is probably difficult to run it outside of the [CSC](https://www.csc.fi)
Puhti computing cluster where it was developed and executed for this project,
and is included primarily for reference purposes to accompany the paper.

That said, in principle the steps to execute it would be:

1) Clone this Git repository

2) Install all prerequisites listed in `conda/deadwood_priority_effects.yaml`,
either using [conda](https://anaconda.org) or by other means.
If using conda, activate the conda environment.

3) Download ProtaxFungi and unzip it into the sister directory

4) Download the raw sequence files (link TBD) into `sequences/01_raw`

5) Download [USEARCH 11.0.667](https://drive5.com/downloads/usearch11.0.667_i86linux32.gz) and put the executable in the `bin` directory.

6) Download [SH matching data from PlutoF](https://files.plutof.ut.ee/public/orig/9C/FD/9CFD7C58956E5331F1497853359E874DEB639B17B04DB264C8828D04FA964A8F.zip) and unzip in `data/sh_matching_data`.

7) In R:

```R
library(targets)
tar_make()
```
