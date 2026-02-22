# Trevor's in-cell FRET data
* ```cells_concat_raw_(1,2).csv``` - raw in-cell datasets concatenated from experimental data from image analysis pipeline ran on microscope images
* ```cells_concat_filtered.csv``` - filtered in-cell dataset produced by dfMake.ipynb
* ```constructs_df.csv``` - aggregated statistics data per-construct produced from cells_concat_filtered data, also in dfMaker.ipynb
* ```invitro.csv``` - data from constructs in-vitro. Folded into constructs_df.csv in dfMaker.ipynb
* ```sequences.csv``` - IDR sequences for GOOSE constructs used for this - figures 2 and 3, in-cell and in-vitro FRET
* ```controls.csv``` - aggregated data from control wells of all experimental plates (7) used for this. Contains MTQ and MNG uncoupled fluorophores, and is used to produce Figsi_ArtifactCorrections.ipynb and FIGsi_PerturbCorrections.ipynb
* ```epsilons.csv``` - calculated epsilons for constructs produced by Finches-sparrow-epsilon.ipynb, folded into constructs_df.csv in dfMaker.ipynb
* ```dfMaker.ipynb``` - filters raw cell dataset to produce figuremaking data
* ```ViolinPlots.ipynb``` - function to create comparative violin plots
* ```FigXX_####.ipynb``` - Figure Panel making scripts - Points to overall figure
* ```Figure_graphs``` - Folder which contains figure plot SVGs
* ```ImageAnalysisScript``` - Folder which contains image analysis script used on raw images to produce cell data concatenated into cells_concat_raw_(1,2).csv