---
layout: default
comments: true
---

# About

Reliability Based Design Optimization (RBDO) allows for the allocation of risk between sub-systems. Typically a RBDO assumes either 

1. You known the statistical distribution
2. You can identify the statistical distribution

which can be very difficult in many practical applications. Often times there is limited data, tests/simulations that are too expensive, or lack of prior knowledge to adequately identify the statistical distribution. 

This challenge aims to motivate the community to explore non-parametric methods that don't require knowledge of the statistical distribution. This will allow RBDO to become more robust in cases where the statistical distribution is not known.

# The challenge

This is a draft of the challenge problem that is subject to change.

![Airplane]({{ "/" | relative_url  }}assets/images/plane.png)

Photograph from <a style="background-color:black;color:white;text-decoration:none;padding:4px 6px;font-family:-apple-system, BlinkMacSystemFont, &quot;San Francisco&quot;, &quot;Helvetica Neue&quot;, Helvetica, Ubuntu, Roboto, Noto, &quot;Segoe UI&quot;, Arial, sans-serif;font-size:12px;font-weight:bold;line-height:1.2;display:inline-block;border-radius:3px" href="https://unsplash.com/@efekurnaz?utm_medium=referral&amp;utm_campaign=photographer-credit&amp;utm_content=creditBadge" target="_blank" rel="noopener noreferrer" title="Download free do whatever you want high-resolution photos from Efe Kurnaz"><span style="display:inline-block;padding:2px 3px"><svg xmlns="http://www.w3.org/2000/svg" style="height:12px;width:auto;position:relative;vertical-align:middle;top:-2px;fill:white" viewBox="0 0 32 32"><title>unsplash-logo</title><path d="M10 9V0h12v9H10zm12 5h10v18H0V14h10v9h12v-9z"></path></svg></span><span style="display:inline-block;padding:2px 3px">Efe Kurnaz</span></a>

We have two panels that are independent of one another (e.g, one on the wing and one on the tail of an airplane). The loads are very well known (deterministic), so the only uncertainties are the failure loads of both panels. One panel is large and therefore heavy, the other panel is small and light. We want to allocate risk between the two so that we have 95% confidence that the probability of failure of the system is less than 10%.

The Objective function is the weight, assumed to be inversely proportional to the stress allowable $$W = W_1/S_{1a}+W_2/S_2a$$, where $$S_{1a}$$ and $$S_{2a}$$ are the allowables (failure strength of the material for each panel).

The design variables are the failure probabilities _p1_ and _p2_ and confidence levels _c1_ and _c2_. 

You will be given some test data on the material strength.

<body>
When $a \ne 0$, there are two solutions to \(ax^2 + bx + c = 0\) and they are
$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$
</body>


# Dates

- 2019/06/01 Initial announcement

# Submission

Coming soon.

# Frequently asked questions

Coming soon.

# Comments

Your feedback is highly appreciated and will help improve the challenge! Feel free to send an email to cjekel@ufl.edu or leave a comment below.
