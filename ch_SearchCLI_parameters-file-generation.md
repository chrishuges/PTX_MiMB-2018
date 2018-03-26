## Parameters file creation

This document describes the creation of a parameters file for analysis of MS files with SearchCLI. 

#### Required software

1. Download SearchGUI from http://compomics.github.io/projects/searchgui.html if not already done.


#### Protocol

1. Navigate to the directory where you want to store your parameters files. 
2. Create your parameters file. This file can be used for an Orbitrap MS2 analysis of TMT 10-plex labeled samples.

	~~~bash
	java -cp /projects/ptx_analysis/chughes/software/software_searchGUI/SearchGUI-3.2.20/SearchGUI-3.2.20.jar eu.isas.searchgui.cmd.IdentificationParametersCLI -out /projects/ptx_analysis/chughes/parameter-files/mar2018/ch_mar2018_OT-MS1_HCD-OT-MS2_human-trypsin_StdMods-TMT10plex.par -db /projects/ptx_analysis/chughes/databases/mar2018/uniprot_human-crap_mar2018_fwd_concatenated_target_decoy.fasta -prec_tol 20 -frag_tol 0.05 -fixed_mods "Carbamidomethylation of C, TMT 10-plex of K, TMT 10-plex of peptide N-term" -variable_mods "Oxidation of M, Acetylation of protein N-term" -db_pi /projects/ptx_analysis/chughes/databases/mar2018/uniprot_human-crap_mar2018_fwd_concatenated_target_decoy.fasta -msgf_instrument 3 -msgf_fragmentation 3 -msgf_protocol 4
	~~~

The parameters file is now created and ready to be used with SearchCLI. 
