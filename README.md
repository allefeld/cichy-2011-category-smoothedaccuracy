# Test data based on Cichy et al. (2011)

This data set, `cichy-2011-category-smoothedaccuracy`,  was
derived from the data acquired by Cichy, Chen & Haynes (*NeuroImage*
2011; used with permission) following the procedure described by
Allefeld, Görgen & Haynes (*NeuroImage* 2016):

> Twelve different visual stimuli belonging to four different categories
> were presented either to the left or the right of fixation (24
> experimental conditions) to N = 12 subjects. There were four different
> trials per condition in each of five different runs. fMRI data were
> recorded from a field of view covering the ventral visual cortex at an
> isotropic resolution of 2 mm. Data were preprocessed and normalized to
> the MNI template. A linear SVM with parameter C = 1 was trained on GLM
> parameter estimates from four of the runs, and tested on the fifth
> run, in a leave-one-run-out cross-validation scheme. Classification
> was pairwise (24 · 23 / 2 = 276 pairs) and accuracies were averaged
> across pairs combining different factor levels, so that the
> chance-level accuracy was a0 = 50 %. For permutation statistics, class
> labels were exchanged in each of the five runs separately, which lead
> to P1 = 2^(5-1) = 16 unique first-level permutations. The analysis
> was performed using a searchlight of radius 4 voxels (comprising 257
> voxels). The resulting accuracy maps were smoothed with a Gaussian
> kernel of 6 mm FWHM.

In particular, these are the results for classification of stimulus
category. The directory has 12 subdirectories corresponding to the
subjects, and each contains 16 files with filenames of the form
`sa_C0002_P####.nii.gz`, where `####` is the index of the permutation.
The index 1 corresponds to the neutral permutation, i.e. unpermuted
data. The files are MR images in gzipped NIfTI format containing the
smoothed accuracy values.

The data set is intended to test the implementation
of ['Permutation-based prevalence inference using the minimum
statistic'](https://github.com/allefeld/prevalence-permutation),
but may be used for other purposes as well.

This data set is copyrighted © 2016 by Carsten Allefeld. It is released
under the terms of the [Open Database
License](http://opendatacommons.org/licenses/odbl/1.0/). Any rights in
individual contents of the database are licensed under the [Database
Contents License](http://opendatacommons.org/licenses/dbcl/1.0/).

