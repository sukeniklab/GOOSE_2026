# Sequencing data and scripts associated with "Sequence-ensemble-function relationships for disordered proteins in live cells"

To generate the figures, clone the repository and run the scripts from within the directory on your computer.  
Scripts to generate data were tested on python 3.13.9. Libraries used in the scripts are pandas, numpy, matplotlib, seaborn, and scipy.stats.  

Directory files are as follows:  

* ```sequencing_data_all.csv```  - combined sequencing output of 5 different independent repeats. The labels are as follows: log2FoldChange_{replicate}, padj_{replicate} (adjusted p value), lfcSE_{replicate} (logfoldchange standard error), base_origin (helps uniquely identify which original template sequence the variant is tied to)
These values were averaged across all 3 repeats and tested for statistical significance. 

    Feature columns are as follows: 
        nardini_{feature}: this is output from NARDINI+ from https://github.com/kierstenruff/RUFF_KING_Grammars_of_IDRs_using_NARDINI-
            note: Z score is normalized to the S. Cerevisiae IDR-ome. 
        cider_{feature}: this is output from CIDER found here: https://pappulab.github.io/localCIDER/
        Sparrow_{feature}: this is output from Sparrow found here: https://github.com/idptools/sparrow

* ```heatmap_r_mean_clustered.csv``` - csv used to generate the spearman r heatmaps for figures 5N and S16. The template name corresponds to base_origin. Features from sequencing_data_all and their spearman r values are reported. 
* ```null_permutation_averaged_results.csv``` - csv used to generate spearman r analysis post shuffling log2FoldChange and padj 100 times, taking the average spearman r per template (base_origin) and feature. Columns include base_origin, feature, r_mean, r_std, is_significant, and n_permutations. 
* ```pioreactor_output.csv``` - csv used to generate Fig_S13. This includes experiment, pioreactor_unit, timestamp, od_reading, angle, channel,timestamp_localtime, and hours_since_experiment_created.
