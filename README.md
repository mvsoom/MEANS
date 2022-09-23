Some example [Pluto](https://github.com/fonsp/Pluto.jl) notebooks to explore
**MEANS** to solve [maximum
entropy](https://en.wikipedia.org/wiki/Principle_of_maximum_entropy) (minimum
Kullback-Leibler divergence) problems with [nested
sampling](https://projecteuclid.org/journals/bayesian-analysis/volume-1/issue-4/Nested-sampling-for-general-Bayesian-computation/10.1214/06-BA127.full).

Out-of-the box, MEANS (maximum entropy as nested sampling) works only in
moderate (dozens to hundreds) dimensions, but in this regime has several
interesting advantages over approximate or MCMC-oriented approaches:
- Nested sampling offers clear convergence criteria and has no "burn-in" phase.
- If there is only one constraint active, one nested sampling run can "map out"
  the entire problem for *any* value of the associated Lagrange multiplier
  $\lambda$.
- The associated evidence (normalizing constant) $\log Z$ and its derivatives
  wrt. the Lagrange multipliers $\nabla_\lambda \log Z$ can be evaluated using
  *automatic differentiation* (that is, it is possible to differentiate through
  an entire nested sampling run!)
- Related measures like the KL divergence and the density of states can be
  estimated.
- Prior information can be included naturally.

The `.html` files are rendered from notebooks and can be visualized by
downloading them or directly via `raw.githack.com`:
- <https://raw.githack.com/mvsoom/MEANS/master/dag.jl.html>
- <https://raw.githack.com/mvsoom/MEANS/master/network.jl.html>
- <https://raw.githack.com/mvsoom/MEANS/master/exponential.jl.html>
- <https://raw.githack.com/mvsoom/MEANS/master/naming.jl.html>
