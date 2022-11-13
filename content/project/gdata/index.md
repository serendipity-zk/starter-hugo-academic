---
# slides: example
url_pdf: ""
summary: |2-
    * We proposed Ally, a novel simulation and characterization infrastructure that enables studying web services’ micro-architecture behaviors using Google applications
    * We identify the main bottleneck as thread oversubscription and low prefetch bandwidth usage.
url_video: ""
date: 2022-10-20
external_link: ""
url_slides: ""
title: Enabling Architectural Simulations and Optimizations of Production Web Services
tags: [Research]
links: []
image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart
url_code: ""
---
Modern web services are pervasive, running across hundreds
of thousands of servers in data centers. Hence, even
a small improvement in server efficiency can achieve significant
financial and environmental benefits. 

Improving server efficiency requires a comprehensive study of production web
services’ micro-architectural behaviors. To this end, we
design Ally, a simulation and characterization infrastructure
that enables studying production web services’ microarchitectural
behaviors using recently-released traces of
widely-used production Google applications. 

We identify and mitigate unique challenges in enabling micro-architectural
simulations of these traces via novel techniques introduced by
Ally. Apart from enabling meaningful research on improving
micro-architectural performance, Ally identifies open-source
applications that represent production behaviors.


Based on the simulation and characterization Ally enables,
we determine key micro-architectural performance bottlenecks
faced by production services, identifying several future optimization
opportunities. As examples, we identify that processors
must (1) handle massive thread oversubscription and
(2) utilize available bandwidth to manage large instruction
and data footprints. Based on our case studies of microarchitectural
optimizations, we evaluate context-driven thread
scheduling and bandwidth-aware hardware prefetching to
eliminate 5% and 28% of cache misses faced by these services.
Ally also motivates other future research directions,
such as reducing the warm-up time for predictors and caches.