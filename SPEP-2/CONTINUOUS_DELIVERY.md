# Leveraging SPEP-2 for Continuous Delivery

I would assert that the [git-flow] model is **great** for situations where you **are not** leveraging _continuous delivery_ or _continuous deployment_. A built-in expectation of this model is that you bundle up your changes and deploy _a release branch_.

This is true for SimplePie, but not necessarily for a _continuous delivery_ or _continuous deployment_ deployment model. If you wanted to adapt this document for that model, I would recommend making the following exemptions:

* The `master` branch should be able to ship to _Production_ at all times.

* Do not use a `develop` branch. Since we are following the continuous deployment pattern, all changes should be small and well-tested.

  [git-flow]: https://github.com/nvie/gitflow
