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


<!-- \mathnote{
The cloud droplet size distribution can be expressed via a Gamma distribution function

$N(D) = N_0 D^\mu \exp(-\Lambda D)$, $0 \le D \le D_{max}$

where $N_0$ [$m^{-3}\; mm^{1-\mu}$], $\mu$, and $\Lambda\; [mm^{-1}]$ are parameters of the distribution, and $D_{max}$ is the maximum drop diameter. The distribution parameters have units of spectral density. A triplet of values for $N_0$ , $\mu$, $\Lambda$  can be fitted to describe measured hydrometeor distributions.
} -->
