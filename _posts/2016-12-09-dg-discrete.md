---
layout: post
title: Interior Penalty Discontinuous Galerkin Methods&#58 The Discrete Problem
img: dgpost.jpg
use_math: true
---

Greetings. Today we are going to write the discrete problem of the inter-element integral in form of the interior penalty discontinuous Galerkin methods for an elliptic problem. Also to do that we will use a notation of differential forms.

The model problem is

$$ -\nabla\lambda\nabla u=f\rightarrow-\delta\lambda du=f$$ in a domain $$\Omega$$ with some boundary conditions $$ u=u_0$$ on $$\partial \Omega$$,

where the function u is a 0-form, $ d$ is the exterior derivative and $ \delta=\star d\star$ is the coderivative operator. For 0-forms $ d$ simply means the gradient of a function.

The discrete problem of an interior penalty discontinuous Galerkin method for an elliptic problem:

$$ (\lambda d_hu_h, d_hv)-\int_\Gamma \left([\lambda u_h]\left<d_hv\right>\mp\left<\lambda d_hu_h\right>[v]\right)\,d\Gamma+\mu\int_\Gamma[u_h][v]\,d\Gamma=(f,v).$$

where $ [\cdot]$ and $ \left<\cdot\right>$ are the operators of jump and average, respectively. Instead of the symbol $ \mp$ one should use $ '-'$ or $ '+'$ to get the symmetric or nonsymmetric discrete problem.

The averages and jumps defines as follows $ [u]=u^jn^j+u^en^e=(u^j-u^e)n^j$ and $ \left<u\right>=\frac{1}{2}(u^j+u^e)$ on an interior boundary $ \Gamma_{je}$ shared by elements $ K_j$ and $ K_e$ and $ n^j$ is the outward normal unit vector to $ \partial K_j$.

Replacing the function $ u$ by $ u=u^j_h\psi_j$ using Einstein notation and rewriting the inter-element integral as

$ (u,v)\rightarrow\int_{\Gamma_{je}}uv\,d\Gamma_{je}$ we obtain the discrete problem

$$ -\int_\Gamma \left([\lambda u_h]\left<d_hv\right>\mp\left<\lambda d_hu_h\right>[v]\right)\,d\Gamma+\mu\int_\Gamma[u_h][v]\,d\Gamma=\\

-\left(([\lambda u_h],\left<d_hv\right>)\mp(\left<\lambda d_hu_h\right>,[v])\right)+\mu([u_h],[v])

=\\-0.5((\lambda^ju^j_kn^j\psi_k^j,d\psi_i^j)+(\lambda^ju^j_k\psi_k^j,d\psi_i^e) -(\lambda^eu_k^e\psi_k^en^j,d\psi_i^j)- (\lambda^eu^e_k\psi^e_kn^j,d\psi_i^e)\mp \\  ((\lambda^ju^k_kd\psi_k^j,\psi^e_jn^j)-(\lambda^ju_k^jd\psi_k^j,\psi_i^en^j)+ (\lambda^eu^e_kd\psi^e_k,\psi^j_in^j)-(\lambda^eu_k^ed\psi_k^e,\psi_i^en^j)))+\\ \mu((u_k^j\psi_k^jn^j,\psi^j_in^j)-(u^j_k\psi^j_kn^j,\psi^e_in^j)-(u^e_k\psi_k^en^j,\psi^j_in^j)+(u^e_k\psi^e_kn^j,\psi^e_in^j)).$$

That is all. Probably, next time we will describe the full process of obtaining the discrete problem from the idea.

Recommended literature

D.N. Arnold, F. Brezzi, B. Cockburn, D. Marini, Unified analysis of discontinuous Galerkin methods for elliptic problems, SIAM J. Numer. Anal., 39 (2002), 1749-1779.
