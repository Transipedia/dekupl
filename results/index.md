---
layout: page
title: Results
permalink: /results/
---

Publication results
-------------------

### EMT experiment

DE-kupl was run using RNA-seq libraries from Yang et al.([1](#references)) retrieved on
the GEO web site under accession [GSE75492](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE75492){:target="_blank"}.

#### Samples
The following Fastq files were used:

SRA_id | condition | timepoint | replicate number
------ | --------- | --------- | ----------------
[GSM1956974](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM1956974){:target="_blank"} | E | No Dox | rep1
[GSM1956975](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM1956975){:target="_blank"} | E | No Dox | rep2
[GSM1956976](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM1956976){:target="_blank"} | E | No Dox | rep3
[GSM1956977](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM1956977){:target="_blank"} | E | Day1 | rep1
[GSM1956978](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM1956978){:target="_blank"} | E | Day1 | rep2
[GSM1956979](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM1956979){:target="_blank"} | E | Day1 | rep3
[GSM1956992](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM1956992){:target="_blank"} | M | Day6 | rep1
[GSM1956993](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM1956993){:target="_blank"} | M | Day6 | rep2
[GSM1956994](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM1956994){:target="_blank"} | M | Day6 | rep3
[GSM1956995](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM1956995){:target="_blank"} | M | Day7 | rep1
[GSM1956996](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM1956996){:target="_blank"} | M | Day7 | rep2
[GSM1956997](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM1956997){:target="_blank"} | M | Day7 | rep3
{: .table }

#### DE-kupl Parameters

DE-kupl was executed with the following parameters:

- min_recurrence: `6`
- min_recurrence_abundance: `5`
- pvalue_threshold: `0.05`
- lib_type: `stranded`
- diff_method: `ttest`
- conditions: `E vs M`


#### Output files

These output files are availabe for download:

Filename | Description
---------|------------
[DiffContigsInfos.tsv.gz]({{ "/results/EMT/DiffContigsInfos.tsv.gz" | prepend: site.baseurl}}) | Contig table
[diff_contigs.bed.gz]({{ "/results/EMT/diff_contigs.bed.gz" | prepend: site.baseurl}}) |  Contig bed file (Human HG38 coordinates)
[ContigsPerLoci.tsv.gz]({{ "/results/EMT/ContigsPerLoci.tsv.gz" | prepend: site.baseurl}}) | Locus table
{: .table }

#### References

(1) Yang Y. et al (2016) Determination of a Comprehensive Alternative
Splicing Regulatory Network and Combinatorial Regulation by Key
Factors during the Epithelial-to-Mesenchymal Transition. Mol Cell Biol
[36:1704-19](https://www.ncbi.nlm.nih.gov/pubmed/27044866).

### GTEx / HPA Cross validation data

#### Output files

Filename | Description
---------|------------
[libraries.txt]({{ "/results/GTEx-vs-HPA/libraries.txt" | prepend: site.baseurl}}) | Description of GTEx and HPA libraries used.
[DiffContigsInfos.tsv.gz]({{ "/results/GTEx-vs-HPA/DiffContigsInfos.tsv.gz" | prepend: site.baseurl}}) | Result of DEkupl run on GTEx data: contig table
[diff_contigs.bed.gz]({{ "/results/GTEx-vs-HPA/diff_contigs.bed.gz" | prepend: site.baseurl}}) | Result of DEkupl run on GTEx data: contig bed file (Human HG38 coordinates)
[gtex.fa]({{ "/results/GTEx-vs-HPA/gtex.fa" | prepend: site.baseurl}}) | Fasta file with selection of representative k-mers for best contigs (higher abs(fold change)) in each category : {::nomarkdown}<ul><li>polyA (100)</li><li>splice (100)</li><li>lincRNA (100)</li><li>intron_DU (100)</li><li>repeat (100)</li><li>unmapped (50)</li></ul>{:/} For each k-mer, the fasta comment line contains: `[event class] [contig #] [mean count Colon] [mean cout Skin] [up or down in Skin]`
