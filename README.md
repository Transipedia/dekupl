# DE-kupl
Exhaustive capture of biological variation in RNA-seq data through k-mer decomposition (article: https://doi.org/10.1186/s13059-017-1372-2, pre-print: http://biorxiv.org/content/early/2017/06/02/122937).

DE-kupl is a computational protocol that aims to capture all k-mer variation in an input set of RNA-seq libraries. This protocol is composed of four main components :

- **Indexing**: index and count all k-mers (k=31) in the input libraries
- **Filtering**: delete k-mers representing potential sequencing errors or perfectly matching known transcripts
- **Differential Expression (DE)**: select k-mers with significantly different abundance across conditions
- **Extension and annotation**: build k-mer contigs and annotate contigs based on sequence alignment.

## Installation and usage

The DE-kupl project is composed of two sub-project: 

- [DE-kupl run](https://github.com/Transipedia/dekupl-run): DE-kupl analysis from raw FASTQ to the table of differentially expressed k-mer contigs (DE contigs). 
- [DE-kupl annotation](https://github.com/Transipedia/dekupl-annotation) Annotates DE contigs produced by DE-kupl run.

Therefore, you need to download and execute both sub-projects.

To avoid installing all dependencies, use our Docker implementation at:
https://hub.docker.com/r/ebio/dekupl/. 
The Docker image is automatically updated everyday. It only contains the DE-kupl run part for now.

**WARNINGS**: Currently DE-kupl, is set up for Human genome only. Manual modification of the sources is needed to handle other species.
