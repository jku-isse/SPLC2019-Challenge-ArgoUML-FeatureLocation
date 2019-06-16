# SPLC2019-Challenge-ArgoUML-FeatureLocation

Artifacts for the paper "Comparison-Based Feature Location in ArgoUML Variants" submitted as solution to the [ArgoUML feature location challenge](https://variability-challenges.github.io/2018/ArgoUMLSPL/index.html) of SPLC.

The [results](https://github.com/jku-isse/SPLC2019-Challenge-ArgoUML-FeatureLocation/tree/master/results) folder contains a subfolder for each of the 15 scenarios of the challenge.
Each scenario folder contains a CSV file with the metrics computed by the challenge benchmark and the corresponding set of traces in the format requested by the challenge.

All that is needed to reproduce the results is available in the [main ECCO repository](https://github.com/jku-isse/ecco/tree/develop).

It contains the [Java adapter implemented for the challenge](https://github.com/jku-isse/ecco/tree/develop/adapter/challenge).

The file [ChallengeTest.java](https://github.com/jku-isse/ecco/tree/develop/adapter/challenge/src/integrationTest/java/at/jku/isse/ecco/adapter/challenge/test/ChallengeTest.java) contains three unit tests:
* Create_Repo: creates the ECCO repository containing all the computed traces.
* Compute_Results: converts the traces stored in ECCO repository in the format requested by the challenge benchmark.
* Analyze_Differences: optional; shows all the differences between the results computed from the ECCO repository and the ground truth results provided by the challenge.
