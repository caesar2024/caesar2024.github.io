+++
title = "Autoconversion"
hascode = true
date = Date(2023, 5, 30)
rss = "Episode X: How do we parameterize autoconversion?"
+++

# What is Autoconversion?

The picture below shows a shallow cloud with rain falling from the center. Observations show that this type of rain can form within 30 min of the initial cloud formation. Autoconversion is the process that transforms small cloud droplets into larger rain drops that then fall out from the base of the cloud.  

![Picture of a raincloud](/assets/raincloud.jpg)

**Figure 1.** Cumulus with likely warm rain falling from the center. Image Credit: Versageek/CC BY-SA 3.0 via Wikimedia Commons.


\concept{
    Autoconversion refers to the initial stage of the collision–coalescence process whereby cloud droplets collide and coalesce to form drizzle drops. Because of the low collection efficiencies among cloud drops, autoconversion can be the limiting factor in the formation of drizzle
}

### Part 1: Representing Cloud Droplet Distributions

A cloud is made of a collection of tiny drops that are 10 to 30 μm in diameter. This is smaller than the width of human hair, which is ~70  μm in diameter. The collection of drops can be summarized as a distribution. Summing over the distribution gives the average number of droplets per unit volume. For example, a typical number concentration is 100 cm⁻³, or 100 droplets in a 1×1×1 cm box. The average droplet diameter μ gives the size of the most common droplets. The dispersion σ gives an approximate range of droplet sizes. The relative dispersion CV, denoting the coefficient of variation, is the ratio of σ/μ and gives the relative width of the distribution. Larger values for CV correspond to broader distributions. You can use the sliders below to explore how these terms change the distribution.

~~~
<div class="myframe1">
<iframe class="responsive-iframe" src="https://caesar2024.github.io/webapps/xowh/"   style="border:none;"></iframe>
</div>
~~~
**Figure 2.** The cloud droplet size distribution. The example data spectra S1 and S2 are taken from Snider and Brenguier (2000).

\exercise{
1. On a piece of paper, predict/sketch how changing Nₜ, μ, and CV change the computed droplet size distribution.
2. Use the sliders to verify your prediction. 
3. Evaluate the standard deviation σ for μ = 20 and CV = 0.2. Use the statistical definition of standard deviation to describe how this value relates to the width of the droplet spectrum.
4. Double-click on "S1" in legend. This will bring up an example cloud droplet spectrum from a stratocumulus cloud deck near the Canary Islands in Spain. Error bars are ±1 standard deviation expressing variability from pooling several spectra from different regions of the cloud. Use the sliders to find the best possible overlap between the model and the data. Record the values for Nₜ, μ, and CV.
5. Repeat this exercise for spectrum "S2". 
6. Contrast the Nₜ, μ, and CV between "S1" and "S2". Write a short paragraph that quantitively summarizes the differences between the two spectra. 
7. Advanced question: The spectrum "S1" corresponds to regions in the cloud where updraft velocities are higher while the spectrum "S2" corresponds to regions in the cloud where updraft velocities are lower. Propose a hypothesis that might explain the differences between S1 and S2.
}

### Part 2: Rain Formation by Autoconversion
The distribtuion of cloud droplets evoles during autoconversion. Collisions of two droplets reduces cloud droplet number concentration. Collisions also produce drops of a larger size. The cloud liquid water content (LWC) is controlled mainly by thermodyamics. The combination of droplet concentration and LWC yields the mean droplet diameter. The CV value determines the dispersion of the distribution as in Figure 2. 


~~~
<div class="myframe2">
<iframe class="responsive-iframe" src="https://caesar2024.github.io/webapps/hjve/"   style="border:none;"></iframe>
</div>
~~~
**Figure 3.** Evolution of cloud and rain liquid water content (LWC), mean rain drop diameter (D) and rain number concentration (N) over time. 



### Part 3: Math Stuff

It is desirable that the size distribution remains describable by a single mathematical function during the entire process. This is called the *main function approach*. The [Gamma distribution probability density function](https://en.wikipedia.org/wiki/Gamma_distribution)  is suitable to characterize autoconversion. 


\mathnote{
$f(x) = A x^\nu \exp(-B x)$

where $A$ ($cm^{-3}\; g^{1-\nu}$), $\nu\; (-)$, and $B\;(g^{-1})$ are parameters of the distribution, and $x$ is the mass of the drop. The distribution $f(x)$ has units of spectral density $cm^{-3}\;g^{-1}$. The integral $\int_0^\infty f(x)dx$ equals the total liquid water mass. A triplet of values for $A$, $\nu$, $B$ can be fitted to describe a measured hydrometeor distribution.
}

While the function above written in terms of mass, measurements are often given in terms of droplet diameter, as shown in Figure 2. The parameters of the mass-based Gamma distribution function can be obtained from the inputs to Figure 1 $N_t$, $\mu$, and $CV$ through mathematical transformation. The $\nu$ paremeter determines the width of the distribution and thus affects the autoconversion rate.  It is related to the coefficient of variation via $\nu \approx 0.112/CV^2 - 1$.

### Part 3: References

Snider, J.R. and Brenguier, J.-L. (2000), Cloud condensation nuclei and cloud droplet measurements during ACE-2. Tellus B, 52: 828-842. [https://onlinelibrary.wiley.com/doi/abs/10.1034/j.1600-0889.2000.00044.x](https://onlinelibrary.wiley.com/doi/abs/10.1034/j.1600-0889.2000.00044.x).