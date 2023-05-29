+++
title = "Autoconversion"
hascode = true
date = Date(2023, 5, 30)
rss = "Episode X: How do we parameterize autoconversion?"
+++

# How do we parameterize autoconversion? 

\concept{
    Autoconversion refers to the initial stage of the collision–coalescence process whereby cloud droplets collide and coalesce to form drizzle drops. Because of the low collection efficiencies among cloud drops, autoconversion can be the limiting factor in the formation of drizzle
}


### Part 1: Representing Cloud Droplet Distributions

~~~
<div class="myframe1">
<iframe class="responsive-iframe" src="https://caesar2024.github.io/webapps/xowh/"   style="border:none;"></iframe>
</div>
~~~
**Figure 1.** The cloud droplet size distribution represented by a Gamma distribution function.



### Part 2: The Main Function Approach

During autoconversion, the size distribution continuously evolves over time. Collisions of two drops reduces cloud droplet number concentration. Collisions also produce drops of a larger size. It is desirable that the size distribution remains describable by a single mathematical function during the entire process. This is called the *main function approach*. The [Gamma distribution probability density function](https://en.wikipedia.org/wiki/Gamma_distribution)  is suitable to characterize autoconversion. 


\mathnote{
$f(x) = A x^\nu \exp(-B D)$

where $A$ ($cm^{-3}\; g^{1-\nu}$), $\nu\; (-)$, and $B\;(g^{-1})$ are parameters of the distribution, and $x$ is the mass of the drop. The distribution $f(x)$ has units of spectral density $cm^{-1}\;g^{-1}$. The integral $\int_0^\infty f(x)df$ equals the total liquid water mass. A triplet of values for $A$, $\nu$, $B$ can be fitted to describe a measured hydrometeor distribution.
}

While the function above written in terms of mass, measurements are often given in terms of droplet diameter, as shown in Figure 1. The parameters of the mass-based Gamma distribution function can be obtained from the inputs to Figure 1 $N_t$, $D_g$, and $CV$ through mathematical transformation. Most importantly, the $\nu$ parameter controls the autoconversion rate. It is related to the coefficient of variation via $\nu \approx 0.112/CV^2 - 1$.
