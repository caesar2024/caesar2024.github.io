+++
title = "Autoconversion"
hascode = true
date = Date(2023, 5, 30)
rss = "Episode X: How do we parameterize autoconversion?"
+++

# What is Autoconversion?

The picture below shows a shallow cloud with rain falling from the center. Observations show that this type of rain can form within 30 min of the initial cloud formation. Autoconversion is the process that transforms small raindrops that make up the cloud into larger drops that then fall out from the base of the cloud.  

![Picture of a raincloud](/assets/raincloud.jpg)

**Figure 1.** Cumulus with likely warm rain falling from the center. Image Credit: Versageek/CC BY-SA 3.0 via Wikimedia Commons.


\concept{
    Autoconversion refers to the initial stage of the collision–coalescence process whereby cloud droplets collide and coalesce to form drizzle drops. Because of the low collection efficiencies among cloud drops, autoconversion can be the limiting factor in the formation of drizzle
}

### Part 1: Representing Cloud Droplet Distributions

A cloud is made of a collection of tiny drops that are 10 to 30 μm in diameter. This is smaller than the width of human hair, which is ~70  μm in diameter. The collection of drops can be summarized as a statistical distribution. The total number concentration gives the average number of droplets per unit volume. For example, a typical number concentration is 100 cm⁻³, or 100 droplets in a 1×1×1 cm box. The average droplet diameter μ gives the size of the most common droplets. The dispersion σ gives an approximate range of droplet sizes. The relative dispersion CV, denoting the coefficient of variation, is the ratio of σ/μ and gives the relative width of the distribution. Larger values for CV correspond to broader distributions. You can use the sliders below to explore how these terms change the distribution.

~~~
<div class="myframe1">
<iframe class="responsive-iframe" src="https://caesar2024.github.io/webapps/xowh/"   style="border:none;"></iframe>
</div>
~~~
**Figure 2.** The cloud droplet size distribution.


### Part 2: Rain Formation by Autoconversion
During autoconversion, the size distribution continuously evolves over time. Collisions of two drops reduces cloud droplet number concentration. Collisions also produce drops of a larger size. The cloud liquid water content (LWC) is controlled mainly by thermodyamics. The combibation of the total drop number concentration and LWC yields the mean droplet diameter. The CV value determines the dispersion of the distribution as in Figure 2. 


~~~
<div class="myframe2">
<iframe class="responsive-iframe" src="https://caesar2024.github.io/webapps/hjve/"   style="border:none;"></iframe>
</div>
~~~
**Figure 3.** Evolution of cloud and rain liquid water content (LWC), mean rain drop diameter (D) and rain number concentration (N) over time. 



### Part 3: Math Stuff

During autoconversion, the size distribution continuously evolves over time. Collisions of two drops reduces cloud droplet number concentration. Collisions also produce drops of a larger size. It is desirable that the size distribution remains describable by a single mathematical function during the entire process. This is called the *main function approach*. The [Gamma distribution probability density function](https://en.wikipedia.org/wiki/Gamma_distribution)  is suitable to characterize autoconversion. 


\mathnote{
$f(x) = A x^\nu \exp(-B D)$

where $A$ ($cm^{-3}\; g^{1-\nu}$), $\nu\; (-)$, and $B\;(g^{-1})$ are parameters of the distribution, and $x$ is the mass of the drop. The distribution $f(x)$ has units of spectral density $cm^{-1}\;g^{-1}$. The integral $\int_0^\infty f(x)df$ equals the total liquid water mass. A triplet of values for $A$, $\nu$, $B$ can be fitted to describe a measured hydrometeor distribution.
}

While the function above written in terms of mass, measurements are often given in terms of droplet diameter, as shown in Figure 2. The parameters of the mass-based Gamma distribution function can be obtained from the inputs to Figure 1 $N_t$, $D_g$, and $CV$ through mathematical transformation. Most importantly, the $\nu$ parameter controls the autoconversion rate. It is related to the coefficient of variation via $\nu \approx 0.112/CV^2 - 1$.
