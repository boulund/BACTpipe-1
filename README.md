[![DOI](https://zenodo.org/badge/83326100.svg)](https://zenodo.org/badge/latestdoi/83326100)

# BACTpipe 
BACTpipe is a whole genome sequencing workflow. It does quality assessment of
paired input reads, tries to assess if the sample contains mixed or pure
isolates, performs *de novo* assembly, and annotates the assembled genome.
BACTpipe uses Nexflow as a workflow manager. 

![BACTpipe flowchart](./docs/source/img/BACTpipe_V3_draft1.png)

## Documentation
Complete documentation is available at https://bactpipe.readthedocs.io. 

## Quick-start
You need to have [Nextflow](https://www.nextflow.io) and Python 3.6+ installed.
The easiest way to get BACTpipe up and running is to install all other
dependencies using [conda](https://conda.io/docs/). The following command
installs the required software:

    conda install java mash bbmap fastqc shovill multiqc 

In order to run the contamination screening step, a mash screen database is
required. Download it from here:

    https://gembox.cbcb.umd.edu/mash/refseq.genomes.k21s1000.msh


## Run BACTpipe
Nextflow makes it easy to run BACTpipe:

    $ nextflow run ctmrbio/BACTpipe --mashscreen_database path/to/refseq.genomes.k21s1000.msh --reads 'path/to/reads/*_R{1,2}.fastq.gz'

This will run BACTpipe locally. For more details on how to run BACTpipe, see
the official documentation at https://bactpipe.readthedocs.io.

## License
BACTpipe is published under the MIT license 2018

## Authors
Joseph Kirangwa (@b16joski), 
Sandra Alvarez-Carretero (@sabifo4),
Fredrik Boulund (@boulund),
Kaisa Thorell (@thorellk)
