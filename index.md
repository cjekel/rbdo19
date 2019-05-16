---
layout: default
comments: true
---

# About

Reliability Based Design Optimization (RBDO) allows for the allocation of risk between sub-systems. Typically a RBDO assumes either 

1. You know the statistical distribution
2. You can identify the statistical distribution

which can be very difficult in many practical applications. Often times there is limited data, tests/simulations that are too expensive, or lack of prior knowledge to adequately identify the statistical distribution. Unfortunately, this means that deterministic regulators (FAA or Mil-Spec) are more rigorous probabilistically than the RBDO community.

This figure highlights the differences between deterministic regulators and the RBDO community.
![Difference between FAA and RBDO]({{ "/" | relative_url  }}assets/images/rbdo.png)
RBDO replaces constraint boundary with distribution (required). FAA (deterministic) replaces it with 10th percentile with 95% confidence even without known distribution.

This challenge aims to motivate the community to explore non-parametric methods that don't require knowledge of the statistical distribution. This will allow RBDO to become more robust in cases where the statistical distribution is not known.

# The challenge

This is a draft of the challenge problem that is subject to change.

![Airplane]({{ "/" | relative_url  }}assets/images/plane.png)

Photograph from <a style="background-color:black;color:white;text-decoration:none;padding:4px 6px;font-family:-apple-system, BlinkMacSystemFont, &quot;San Francisco&quot;, &quot;Helvetica Neue&quot;, Helvetica, Ubuntu, Roboto, Noto, &quot;Segoe UI&quot;, Arial, sans-serif;font-size:12px;font-weight:bold;line-height:1.2;display:inline-block;border-radius:3px" href="https://unsplash.com/@efekurnaz?utm_medium=referral&amp;utm_campaign=photographer-credit&amp;utm_content=creditBadge" target="_blank" rel="noopener noreferrer" title="Download free do whatever you want high-resolution photos from Efe Kurnaz"><span style="display:inline-block;padding:2px 3px"><svg xmlns="http://www.w3.org/2000/svg" style="height:12px;width:auto;position:relative;vertical-align:middle;top:-2px;fill:white" viewBox="0 0 32 32"><title>unsplash-logo</title><path d="M10 9V0h12v9H10zm12 5h10v18H0V14h10v9h12v-9z"></path></svg></span><span style="display:inline-block;padding:2px 3px">Efe Kurnaz</span></a>

We have two panels that are independent of one another (e.g, one on the wing and one on the tail of an airplane). The loads are very well known (deterministic), so the only uncertainties are the failure loads of both panels. One panel is large and therefore heavy, the other panel is small and light. We want to allocate risk between the two so that we have 95% confidence that the probability of failure of the system is less than 10%.

The Objective function is the weight, assumed to be inversely proportional to the stress allowable $$W = W_1/S_{1a}+W_2/S_2a$$, where $$S_{1a}$$ and $$S_{2a}$$ are the allowables (failure strength of the material for each panel).

The design variables are the failure probabilities $$p_1$$ and $$p_2$$ and confidence levels $$c_1$$ and $$c_2$$. Essentially the failure allowables are expressed as a function of the probability and confidence level (e.g. $$S_{1a}(p_1, c_1)$$ and $$S_{1a}(p_1, c_1)$$)

You will be given some test data on the material strength ($$S_1, S_2$$) in order to calculate the allowables. A typical RBDO would require that you identify the distribution that the material strength follows, however there isn't enough test data or prior knowledge to do this. The challenge will assume that the material strength data belongs to the log-concave CDF distribution class. The test data you'll be given will be the first and fifth lowest failure strength of the material, which was collected from six total tests. See [1](https://jekel.me/rbdo19/#1) to calculate $$S_{1a}$$ and $$S_{2a}$$ from this data for a given probability and confidence level for the log-concave CDF distribution class.

The goal is to allocate risk between two independent panels for 95% confidence that system probability of failure is less than 10%.

# Dates

- 2019/05/22 Initial announcement

# Submission

Coming soon.

# Frequently asked questions

Coming soon.

# References

### 1
Hanson, D. L.; Koopmans, L. H. Tolerance Limits for the Class of Distributions with Increasing Hazard Rates. Ann. Math. Statist. 35 (1964), no. 4, 1561--1570. doi:10.1214/aoms/1177700380. [https://projecteuclid.org/euclid.aoms/1177700380](https://projecteuclid.org/euclid.aoms/1177700380)

# Comments

Your feedback is highly appreciated and will help improve the challenge! Feel free to send an email to cjekel@ufl.edu or leave a comment below.
