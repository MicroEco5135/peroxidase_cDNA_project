README for trees		created by EE on 07.31.2017
________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
Purpose: provides fat-branch and heat trees phylogenetic trees constructed with RaxML and pplacer generated for our manuscript: Entwistle, E.M., K.J. Romanowicz, W.A. Argiroff, Z.B. Freedman, J.J. Morris, & D.R. Zak. Anthropogenic N deposition alters composition of expressed fungal peroxidases in the forest floor. In preparation.

Background: 
We constructed a guide tree of fungal peroxidase reference sequences obtained from the KEGG, MycoCosm, FunGene, and GenBank databases.  
We sequenced expressed fungal peroxidases from the forest floor of a long-term N deposition experiment: http://webpages.uidaho.edu/nitrogen-gradient/
We placed forest floor expressed peroxidase sequences into our guide tree with pplacer. 
We constructed fat-branch trees of fungal peroxidases occurring only under ambient or experimental N deposition & fat-branch heat-trees comparing fungal peroxidases expressed under ambient and experimental N deposition.
This was done by adapting the KEGGur pipeline (https://github.com/syntherzukal/KEGGUR; Morris, et al. J. Plankton Res. (2016) 38(4): 1103–1114. doi:10.1093/plankt/fbw016), which was originally created for examining catalases & peroxidases for marine metatranscriptomes, for analysis of expressed fungal peroxidase data.
In our manuscript, we display a single representative tree for ambient N deposition, experimental N deposition, and heat trees.  Here, we provide raw, unedited output trees for all 9 iterations of our jackknifed analysis.
In our manuscript, we display our rooted, edited guide tree.  Here, we provide the unedited, unrooted guide tree of fungal peroxidase reference sequences which we used to guide phylogenetic placement of our peroxidase cDNA sequences in KEGGur.
___________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
Subfolders - description:
ambient_trees		-	fat-branch phylogenetic trees of peroxidases expressed under ambient N depositon for all 9 iterations of our jacknifed analysis
experimental_trees	-	fat-branch phylogenetic trees of peroxidases expressed under experimental N depositon for all 9 iterations of our jacknifed analysis
heat_trees			-	fat-branch heat trees comparing fungal peroxidases expressed under ambient & experimental N deposition
guide_tree			-	bootstrapped phylogentic tree of fungal peroxidase reference sequences which we used to guide placement of our cDNA sequences
____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
Viewing notes:

The bootstrapped guide tree should be viewed in a tree-viewing program which can display trees with bootstrap values (MEGA, Geneious, etc.)

To view fat-branch trees, you will need the Archaeopteryx tree-viewing software:  https://sites.google.com/site/cmzmasek/home/software/archaeopteryx

In fat-branch trees, thickness of branches indicates the number of cDNA sequences placed at this branch.

For heat-trees, colored branches indicate differential abundance of sequences at this branch for one treatment over the other.  In Archaeopteryx, the default color scheme for fat-branch heat trees is red and green.  Branches differentially representing ambient N deposition peroxidases are red; branches differentially representing experimental N deposition peroxidases are green.

In file names, v1 through v9 refers to the iterations of our jackknifed analysis.  Files of the same v number are from the same run.  See our manuscript for more details.

Trees presented here are raw, unrooted, and unpruned.  The outgroup for those who wish to root the trees is the clade of peroxidases from the Ascomycota species (i.e., Bipolaris, Pyrenophora, Zymoseptoria, Verticillium, etc.).

_________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________