# LTA Frailty

**Latent transition analysis (LTA) is analysed using LatentGOLD Syntax.**

Syntax is provided in text files. While using LatentGOLD, user should copy syntax to LatentGOLD.

Syntax needs to be run in sequential order:

**1. Latent Class Analysis: to find homogeneous underlying subgroups given indicators, using cross sectional data.**

  1.1. LCA_standard: Standard LCA, with the assumption that within a class, the observed indicators are statistically independent of each other (i.e., local/conditional independence).

  1.2. LCA_LocalDependence: The local dependence assumption is not always possible to be met. It's practically reasonable to relax the assumption, by adding residual correlation between indicators. The pairs of indicators requiring residual correlation are decided by bivariate residuals.

  1.3. LCA_LocalDependence_DIF: With covariates included in the model, differential item functioning needs to be checked and addressed.

**2. LTA: transition between latent classes over time**

  There are 2 main approaches: one-step modeling vs. three-step modeling. 
  
  Here I use three-step modeling strategy: (a) Step 1 and 2 - identify latent classes from longitudinal data, (b) Step 3 - a Markov model.

  2.1. LTA_MI: LTA with measurement invariance assumed

  2.2. LTA_nonMI: LTA without assuming measurement invariance

  By comparing goodness-of-fit indices, I decide if MI assumption is valid. The resultant latent classes of chosen LTA model is saved for Step 3.

  2.3. LTA_step 3: The resultant classes are fitted into a Markov model, assuming stationary.
