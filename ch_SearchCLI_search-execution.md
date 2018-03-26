##SeachCLI execution

This document describes execution of a search using SearchCLI. 

####Required software

1. Download SearchGUI from http://compomics.github.io/projects/searchgui.html if not already done.


####Protocol

1. Navigate to the directory where you have stored your MGF files generated in RawQuant.
2. Start the SearchCLI process. The -Xmx flag here specifies the amount of RAM. Alter based on your system.

	~~~bash
	for i in *.mgf; do java -Xmx300g -cp /projects/ptx_analysis/chughes/software/software_searchGUI/SearchGUI-3.2.20/SearchGUI-3.2.20.jar eu.isas.searchgui.cmd.SearchCLI -spectrum_files /projects/ptx_analysis/chughes/projects-current/test-project/mgf/$i -output_folder /projects/ptx_analysis/chughes/projects-current/test-project/search-output/ -id_params /projects/ptx_analysis/chughes/parameter-files/mar2018/ch_mar2018_OT-MS1_HCD-OT-MS2_human-trypsin_StdMods-TMT10plex.par -output_option 1 -xtandem 1 -myrimatch 1 -msgf 1 -comet 1; done
	~~~

The search should loop through all mgf files in the directory and make an individual zipped output of the results for each. 
