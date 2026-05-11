# Trevor's in-cell FRET data
* ```cells_concat_raw_(1,2).csv``` - raw in-cell datasets concatenated from experimental data from image analysis pipeline ran on microscope images
* ```cells_concat_filtered.csv``` - filtered in-cell dataset produced by dfMaker.ipynb
* ```constructs_df.csv``` - aggregated statistics data per-construct produced from cells_concat_filtered data, also in dfMaker.ipynb
* ```constructs_df_sim.csv``` - aggregated statistics data per-construct produced by MD simulations for net-positively charged sequences
* ```invitro.csv``` - data from constructs in-vitro. Folded into constructs_df.csv in dfMaker.ipynb
* ```sequences.csv``` - IDR sequences for GOOSE constructs used for this - figures 2 and 3, in-cell and in-vitro FRET
* ```controls.csv``` - aggregated data from control wells of all experimental plates (7) used for this. Contains MTQ and MNG uncoupled fluorophores, and is used to produce Figsi_ArtifactCorrections.ipynb and FIGsi_PerturbCorrections.ipynb
* ```epsilons.csv``` - calculated epsilons for constructs produced by Finches-sparrow-epsilon.ipynb, folded into constructs_df.csv in dfMaker.ipynb
* ```dfMaker.ipynb``` - filters raw cell dataset to produce figuremaking data- makes cells_concat_filtered.csv and constructs_df.csv
* ```GOOSE_ChargedxPcount_kappa_library_measured.csv``` - contains ~3000 GOOSE-generated sequences and measured characteristics (pcount, FCR, etc.) for the proline titration test in Fig_ED3
* ```ImageAnalysisScript``` - Image analysis script used on raw images to produce cell data concatenated into cells_concat_raw_(1,2).csv