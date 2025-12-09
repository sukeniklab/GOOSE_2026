# Sequencing data and scripts associated with "Sequence-ensemble-function relationships for disordered proteins in live cells"

To generate the figures, clone the repository and run the scripts from within the directory on your computer.  
Scripts to generate data were tested on python 3.13.9. Libraries used in the scripts are pandas, numpy, matplotlib, seaborn, and scipy.stats.  

Directory files are as follows:  

"sequencing_data_all.csv" - combined sequencing output of 5 different independent repeats. The labels are as follows: log2FoldChange_{replicate}, padj_{replicate} (adjusted p value), lfcSE_{replicate} (logfoldchange standard error), base_origin (helps uniquiely identify which original WT sequence the variant is tied to)
These values were averaged across all 5 repeats and tested for statistical significance. 

    Feature columns are as follows: 
        nardini_{feature}: this is output from NARDINI+ from https://github.com/kierstenruff/RUFF_KING_Grammars_of_IDRs_using_NARDINI-
            note: Z score is normalized to the S. Cerevisiae IDR-ome. 
        cider_{feature}: this is output from CIDER found here: https://pappulab.github.io/localCIDER/
        Sparrow_{feature}: this is output from Sparrow found here: https://github.com/idptools/sparrow

"heatmap_fig.ipynb" - python script used to generate all heatmaps found in figure 5. 

"volcano_fig.ipynb" - python script used to generate the volcano plot found in figure 5C
