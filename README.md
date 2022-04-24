# slicer_2_bids
Convert clinical imaging data (the 'slicer files') to BIDS-compatible dataset.


The input data is the clinical imaging data for SEEG patients derived from:
(a) structural MRI data
  - All images in files with 'reg' in filenames indicates that the images in the file are registered to the preoperative CT angiogram
(b) EEG contact locations

The output includes:
(a) BIDS-compatible directory and imaging data
  - native space (i.e. in preop CTA space)
  - normalised* space (suffix is '_normalised')

*Normalisation with ANTS to the nihpd_sym_04.5-18.5_nifti template (T1W). See more here: http://nist.mni.mcgill.ca/pediatric-atlases-4-5-18-5y/
