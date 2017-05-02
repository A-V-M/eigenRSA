# eigen distance matrix analysis

Background
==========

The procedure is closely akin to the standard ‘searchlight’ analysis (Kriegeskorte et al, 2008). The key difference is that there is an additional step for this method which involved the decomposition of the pattern into its constituent components (singular value decomposition). The aim of this step was to ascertain which aspects of the pattern are the most relevant in representing a particular type of information.  The resulting components capture different aspects of the pattern’s representational structure. I then converted each of the components into a distance vector by computing the absolute difference between each possible pair of values within a component. This resulted in a set of eigen-RDMs which I then used as predictors in a regression after normalisation to unit length. 

The first component captures the overall summed activity of a pattern. This means that model-RDMs which score highly on this component (i.e. high β-values) are mostly represented within the summed activation of the pattern (as opposed to distributed coding; Trappenberg, 2009). This is an important property to take into account when trying to investigate whether the brain encodes different types of information in different ways. A strong assumption of this method is that voxel responses follow a Gaussian distribution which might not necessarily be the case (Ashby, 2011). Alternatively, independent components analysis (ICA) could potentially be used instead of SVD which does not make such assumptions regarding the nature of statistical dependencies (Hyvärinen et al, 2001). I specifically chose SVD in this case because of its intuitive simplicity and practicality.
