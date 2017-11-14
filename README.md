# MHC fine-mapping in juvenile idiopathic arthritis (JIA)-associated uveitis

Scripts and data used in analyses for "An amino acid motif in HLA-DRβ1 distinguishes patients with uveitis in juvenile idiopathic arthritis."

This repository contains:

#### run_qc.sh

A bash script containing a series of Plink commands used to run sample and variant QC

#### run_smartPCA.sh

Please see the Afib-Stroke-Overlap repository for this script. It uses EIGENSTRAT (https://www.hsph.harvard.edu/alkes-price/eigensoft-frequently-asked-questions/ to run principal component analysis (PCA) either using a reference set of data or just in your own samples.

Usage:   
```./run_smartPCA.sh data_prefix```

#### prephase.sh

A bash script to call SHAPEIT, which will phase your data before imputation.

Usage:   
```./prephase.sh chromosome```

#### impute.sh

A bash script to call IMPUTE2, which will impute your phased data (produced by SHAPEIT)

Usage:   
```./impute.sh chromosome window_start window_stop```

#### impute.chrX.sh

A bash script to call IMPUTE2, which will impute your phased data (produced by SHAPEIT) specifically for the X chromosome

Usage:   
```./impute.sh chromosome window_start window_stop```

#### run_gwas.sh

A bash script that will point Plink to the imputed data and run a genome-wide association study

Usage:   
```./run_gwas.sh chromosome phenotype window_start window_stop```
