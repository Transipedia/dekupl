# DE-kupl
Exhaustive capture of biological variation in RNA-seq data through k-mer decomposition (http://biorxiv.org/content/early/2017/06/02/122937).

DE-kupl is a computational protocol that aims to capture all k-mer variation in an input set of RNA-seq libraries. This protocol is composed of four main components :

- **Indexing**: index and count all k-mers (k=31) in the input libraries
- **Filtering**: delete k-mers representing potential sequencing errors or perfectly matching known transcripts
- **Differential Expression (DE)**: select k-mers with significantly different abundance across conditions
- **Assembly and annotation**: build contigs of assembled k-mers and annotate contigs based on sequence alignment.

## Installation and usage

The DE-kupl project is composed of two sub-project: 

- [DE-kupl run](https://github.com/Transipedia/dekupl-run) which handle the DE-kupl procude from raw FASTQ to the assembly of differentially expressed k-mers. 
- [DE-kupl annotation](https://github.com/Transipedia/dekupl-annotation) which annotate DE contigs produced bu DE-kupl run.

Therfore, you need to download and execute both sub-projects.

**WARNINGS**: Currently DE-kupl, is set up for Human genome only. Manual modification of the sources is needed to handle other species.
