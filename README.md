# EmbeddedAMP
Computer-based method to identify antimicrobial peptides embedded in proteins


This repository contains codes and datasets used in the work entitled "Embedded-AMP: A distributed computational method for the systematic identification of antimicrobial peptides embedded in protein sequences" by German Melendrez Carballo, Karen Guerrero Vazquez, Gabriel Del Rio amd Carlos A. Brizuela.

Three sets of codes are available in this site: InPep, SVMAMP and CAMPred. 

1. InPep solves the problem of identifying non-redudant k-mers (peptides) embedded in the proteins of a proteome.

2. SVMAMP is a support vector machine trained to identify antimicrobial peptides (AMP)

3. CAMPred sends requests to the CAMP web server to predict which k-mer classified by SVMAMP are validated as AMP.

We also provide the AMP/non-AMP used to train SVMAMP and the proteomes that were used to validate the efficiency of these codes.

In each code directory you will find the instructions to compile as well as the code dependencies and versions required.

If you have any questions or are interesting in supporting our work, please contact us at:

- Dr. Carlos Brizuela (cbrizuel@cicese.edu.mx )

- Dr. Gabriel Del Rio (gdelrio@ifc.unam.mx)
