README for expressed fungal peroxidase peroxidase analysis		created by: EE	on	07.28.2017
______________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

Purpose: to provide the code and files neccessary to reproduce the bioinformatic and statistical analyses in our manuscript & to provide access to all phylogenetic trees generated in our analyses

If you use code, sequences, or files provided here, please cite: Entwistle, E.M., K.J. Romanowicz, W.A. Argiroff, Z. Freedman, J.J. Morris, & D.R. Zak. Anthropogenic N deposition alters composition of expressed fungal peroxidases in the forest floor. In preparation.  Please also appropriately cite the relevant programs/packages/databases which we cite in our manuscript. 

If you use the KEGGur pipeline, please additionally cite: Morris, J.J., Z.I. Johnson, S.W. Wilhelm, & E.R. Zinser. Diel regulation of hydrogen peroxide defenses by open ocean microbial communities. J. Plankton Res. (2016) 38(4): 1103–1114. doi:10.1093/plankt/fbw016
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
Subfolder	-	description:
pipelines		-	text files containing commands & instructions for bioinformatic & statistical analyses 
accessory files	-	files needed to run the pipelines, with the exception of sequencing files (see below)
trees			-	output from KEGGur pipeline	including trees of expressed fungal peroxidases from ambient and experimental N deposition treatments and heat trees displaying differences between treatments
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
Pipeline files	-	description: 
perox_pipeline_seqs_tree.txt		- 	sequence processing and and preparation of fasta and count files that for phylogenetic analysis
perox_pipeline_otu.txt				-	nucleotide sequence processing, OTU-clustering, and preparation of files used in analysis of OTU richness and composition
perox_translation.txt				-	instructions on how to translate peroxidase nucleotide sequences into amino acid sequences and determine peroxidase type (i.e., MnP, LiP, VP, GP).
R_analyses.txt						-	provides R commands for comparisons of peroxidase type and peroxidase OTU richness & composition under ambient and experimental N deposition
MnPeroxidase_KEGGur_commands.txt	- 	KEGGur pipeline commands for obtaining reference sequences from the KEGG database, sequence alignment, blastx queries, phylogenetic tree construction and sequence placement, statistical analysis in pplacer
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
Accessory files provided	- 	description:
MC_trimmed.fasta												-	file of the 10 original plasmid insert sequences for our mock community from which primers have been trimmed
fungal_perox_amino_acid_ref_seqs_unaligned.fasta				-	unaligned fungal class II peroxidase amino acid reference sequences, not trimmed
fungal_perox_in_silico_PCR_DB.fasta								-	file of MnP, LiP, and VP fungal peroxidase sequences that we used for in silico PCR to help us design and evaluate the primers used in this manuscript
fungal_peroxidase_nt_ref_alignment.fasta  	 					-	reference alignment for aligning fungal peroxidase cDNA sequences in mothur
perox.env.txt	 												-	environment file providing treatment and site information for each sample for analyses in R
perox1.oligos   												-	provides primers and barcodes for sequences in perox1a.fastq & perox1b.fastq
perox2.oligos	 												-	provides primers and barcodes for sequences in perox2a.fastq & perox2b.fastq
perox3.oligos	 												-	provides primers and barcodes for sequences in perox3a.fastq & perox3b.fastq	
perox4.oligos													-	provides primers and barcodes for sequences in perox4a.fastq & perox4b.fastq
perox5.oligos													-	provides primers and barcodes for sequences in perox5a.fastq & perox5b.fastq
perox6.oligos   												-	provides primers and barcodes for sequences in perox6a.fastq & perox6b.fastq
treatment.design												-	design file providing treatment information for each sample for analyses in mothur
trimmed_fungal_perox_amino_acid_ref_seqs_unaligned.fasta		-	unaligned fungal class II peroxidase amino acid reference sequences, trimmed at primer regions, for guiding translation of fungal peroxidase cDNA OTU sequences in Fungene
_______________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
Sequence availability: 
In order to run the analyses here, you must first obtain our sequence files: perox1a.fastq, perox1b.fastq, perox2a.fastq, perox2b.fastq, perox3a.fastq, perox3b.fastq, perox4a.fastq, perox4b.fastq, perox5a.fastq, perox5b.fastq, perox6a.fastq, perox6b.fastq.
These files are available in the NCBI SRA database in BioProject PRJNA222775 under BioSample accession numbers SAMN07411552 - SAMN07411557.
Notes: 
	1) We ran two rounds of PacBio sequencing per chip, denoted as a and b in the fastq files, in order to generate a sufficient number of sequences for analysis. Files for both rounds of
	sequencing for the same samples have the same BioSample accession number in NCBI (e.g., perox1a.fastq & perox1b.fastq are both available at SAMN07411552).
	2) We added mock community DNA to all PacBio sequencing chips except for perox3. To make analysis less computationally expensive, however, we included barcodes for the mock
	community in the perox2.oligos file only. Mock community DNA for perox1, perox4, perox5, and perox6 uses this same barcode.  Do not be alarmed by unusually high sequence loss at
	the trim.seqs step for these chips as this simply reflects the exclusion of the mock community from the oligos file for those chips.
________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
KEGGur:
Code and annotations for KEGGur are available at https://github.com/syntherzukal/KEGGUR.
________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
Programs and packages used:
1.  mothur (v.1.34.4)
		uchime
2.  R studio
3.  R
		VennDiagram
		vegan
4.  Framebot (run through online portal at http://fungene.cme.msu.edu/FunGenePipeline/framebot/form.spr)
5.  Geneious (v.6.1.8)
		MAFFT multiple alignment plug-in
		Primer3
6.	KEGGur
		Perl
		MUSCLE
		RaxML
		pplacer
		Archaeopteryx tree-viewer

WARNINGS: Run mothur pipelines in separate folders to prevent previously generated files from being overrwritten.  Mothur pipelines were written to function with mothur 1.34.4.  Some commands fail to execute properly in newer versions of mothur.		
__________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

