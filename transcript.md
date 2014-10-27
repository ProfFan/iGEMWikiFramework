#Script - Fan
## gRNA Part
Let me introduce our gRNA design to you.
Our process mainly consists of three steps:  

* First, we screen the full genome collection of the virus to find all possible 23bp sequence within conserved regions.
*  Then we run BLAST against the Human Genome to search for possible off-target sites, and rate them using Zhang's method.
* Finally we use the RNAfold utility to analyze the secondary structure of the sequences in the 2nd step, to make sure that the gRNA binds with Cas9 effectively.

We have designed a few gRNAs for two retroviruses, namely HIV and HBV. For the highly-mutated HIV, we have only found gRNAs with about 50% strain coverage. For HBV, one gRNA with 100% strain coverage has been discovered. Those 50% coverage gRNAs have clear benefits, as they have better ratings and lower off-target effect. Moreover, by combining 2 to 3 such guides, an overall coverage of 100% can be achieved.

## Modelling

As you all know, the gold standard in determining the quality of a model is to compare with the reality.
So let me first show you the real case.
**Show the "The Reality" slide**
Here you can see a figure depicting the progression of AIDS, quoted from Primer to the Immune Response. Basically it has three stages, first is Acute infection, then Clinical Latency, and finally, Acquired immunodeficiency syndrome. As you can see here, there is a huge drop in the number of CD4+ T Cells here.

In our model, we mainly focus on the latter two stages of HIV infection.
**Switch to the next slide**
This is our simulation results with no CRISPR system inside the patient. You may notice that the curve looks extremely similar with the actual case, With a quasi-equilibrium for a long time, and a sudden collapse in the end. We believe that this is a strong indicator that the dynamics of our system is almost identical to the original system.
**Switch to the next slide**
Well there would be a different story if we have introduced our CRISPR system into it. You can see here that the super CD4+ cells took back the dominance and finally the immune system is recovered.
**Next**
We have also analysed the final chance of saving a patient. The result shows that there exists a critical point where everything would be too late for the patient.
