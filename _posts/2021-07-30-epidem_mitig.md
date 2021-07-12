---
title: "Epidemic Tracing for Epidemic Mitigation"
date: 2021-07-30
featured: true
layout: service
authors: sibyl-team
---

Since the beginning of the SARS-CoV-2 pandemic, the strategy of tracking, testing, and isolating people who had contact with COVID-19 positive individuals has proven effective in mitigating the epidemic’s spreading.

Manual contact tracing is an extremely expensive process from the organizational and economic points of view. Manual tracking is effective in the early stages of the epidemic but becomes impractical as the number and size of epidemic outbreaks increase. Therefore, it is useful to combine the manual method with an automatic tracing technique, called digital contact tracing, which consists of the detection and notification via smartphones of contact with a positive tested infected individual in the last two weeks \[[Ferretti, et al.](https://science.sciencemag.org/content/368/6491/eabb6936)\]
. The validity of this approach for epidemic containment has been verified in different contexts, in particular in the UK it is estimated that digital contact tracing has allowed the notification of more than 500 thousand infected people during the second wave, reducing it by a quarter \[[Wymant , et al.](https://www.nature.com/articles/s41586-021-03606-z)\]. Digital contact tracing, however, is not immune from problems in particularly widespread epidemic regimes: a large number of people may be notified of the contact, overloading the tracing system and, consequently, causing a slowdown in the process of testing and isolation of infected individuals.
As an alternative to the notification of contact with a positive person (contact tracing), adopted in the most common digital tracking apps, it is possible to base the testing and isolation strategies on a more accurate estimate of the individual risk of infection (risk assessment). The estimate of the individual risk of infection depends not only on direct contact with positive tested individuals but also on indirect involvement in more complex chains of contagion, which can be reconstructed with techniques borrowed from the statistical physics of complex systems and based on probabilistic modeling of epidemic evolution.


In the following infographic, the operation scheme of the two tracking systems, Digital Contact Tracing and Risk Tracing is shown. In the first case, people who had contact, in recent weeks, with positive tested individuals [indicated in dark orange] receive a notification through the tracking app on their smartphones [red notification icon]. In the second case, the knowledge of the positive tests, but also of the negative ones [indicated in dark blue], allows calculating, for each person equipped with the tracking app, a risk value associated with the epidemic reconstruction, [shown schematically by vertical bar]. Thanks to the probabilistic reconstruction of the chains of contagion, an individual who has a high risk of being infected can be identified even if he has not previously been exposed to positive cases, ensuring greater effectiveness in containing the infection.

![shema](/images/posts/epi_mitig/image4.png)

The techniques presented in this latest work by the Sibyl team and the SmartData@PoliTO center of the Polytechnic of Turin in collaboration with ENS of Paris, the EPFL of Lausanne, and the ICTP of Trieste, continue the research of the SIBYL project funded by the foundation CRT and allow an estimate of the risk of each individual of being infected calculated based on the observations and contacts accumulated in the previous days. The proposed algorithms have the advantage of operating in a distributed manner, allowing implementation on smartphone apps. The proposed system does not require a central computing server or memory storage, making possible solutions that preserve privacy.



The tracking and containment of epidemic spread are dynamic processes that influence each other. The tracing based on the calculation of the epidemic risk guarantees a greater ability to identify the infected, consequently also improving the quantity and quality of the data that the same algorithm will have available to carry out the epidemic reconstruction at subsequent times. The result is a virtuous mechanism in which the efficiency of the tracing process increases over time as well as the containment capacity of the epidemic.
Furthermore, unlike simple contact tracing, this tracking method uses all the information present in the data available, so even the knowledge of negative tests helps to make the estimation of individual risk more accurate. In the video animation below it is shown, on a simplified example, how the epidemic mitigation intervention based on epidemic reconstruction techniques (Risk Tracing) is effective in containing a virtual epidemic, where digital contact tracing fails instead:


![shema](/images/posts/epi_mitig/image3.gif)

**Comparison [on a simplified system for visualization reasons] of the performance in the containment of an epidemic spread between Contact Tracing and Risk Tracing.**

An epidemic simulator developed by the University of Oxford (openABM) was used to verify the effectiveness of the proposed approach. OpenABM allows simulating a realistic spread of a SARS-CoV-2 epidemic in a population of millions of people. The following plots show the evolution of the number of daily infected people in a population of 500,000 individuals, depending on the number of daily tests available. Even with a very limited number of daily tests, the proposed Risk Tracing methods (SMF and BP) can contain the simulated SARS-CoV-2 epidemic, despite the failure of classic digital contact tracing (CT):


![shema](/images/posts/epi_mitig/image1.png)

In the work recently published in the PNAS journal, the robustness of the proposed methods with respect, for example, to limited adoption of the app in the population, the ability to correctly measure contacts between people, and the real channels of contagion were investigated. Even increasing disturbing factors, the results of the Risk Tracing methods show a high degree of stability. In the example shown below, it can be seen that one of the proposed methods (BP) continues to obtain excellent results in epidemic containment even in the presence of tests with a high false-negative value (FNR), such as rapid tests:

![shema](/images/posts/epi_mitig/image2.png)

The published work aims to demonstrate how digital contact tracing (and the apps that implement it) can be improved with small and low budget modifications, to achieve a greater impact on the mitigation of the epidemic spread of SARS-CoV-2 and possible future epidemics. The algorithms and code used were released on an online repository [epidemic_mitigation](https://github.com/sibyl-team/epidemic_mitigation).




