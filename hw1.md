Q1: mkdir xxx
Q2: find . -maxdepth 1 -type d | wc -l

For HW1
grep -v '^#' human.genes.gtf|wc -l
 2575494

 #to get all lines which has the gene_biotype as protein coding 
grep 'gene_biotype "protein_coding"' human.genes.gtf|wc -l
 2351933
 #to get all exon which has the gene_biotype as protein coding 
grep 'gene_biotype "protein_coding"' human.genes.gtf | grep -w 'exon' | wc -l 
1051452

grep 'gene_biotype "protein_coding"' human.genes.gtf | grep -w 'CDS' | awk '{print $1}' | sort | uniq -c

grep 'gene_biotype "protein_coding"' human.genes.gtf | grep -o 'gene_id "[^"]*"' | sort | uniq | wc -l
19961
