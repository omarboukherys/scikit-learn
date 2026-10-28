- :class:`discriminant_analysis.LinearDiscriminantAnalysis` with `solver="svd"` now
  weights the within-class covariance by the class `priors`, like the `"lsqr"` and
  `"eigen"` solvers and as documented for `covariance_`. Previously it weighted the
  classes by their proportions in the training data, so when `priors` differed from
  those proportions, its `predict_proba`, `decision_function` and `predict`
  disagreed with the other solvers.
  By :user:`Omar BOUKHERYS omarboukherys`.
