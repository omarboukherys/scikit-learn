- :class:`discriminant_analysis.LinearDiscriminantAnalysis` with `solver="lsqr"` or
  `solver="eigen"` now weights the class covariances by the class proportions when
  estimating the within-class covariance, as `solver="svd"` already did, instead of
  by `priors`. This is the maximum likelihood estimate. When `priors` differ from the
  class proportions, the three solvers now give the same predictions, and
  `explained_variance_ratio_` of the `"eigen"` solver is always between 0 and 1.
  `covariance_` no longer depends on `priors`.
  By :user:`Omar Boukherys <omarboukherys>`.
