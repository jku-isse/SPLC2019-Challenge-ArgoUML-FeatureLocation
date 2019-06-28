# SPLC2019-Challenge-ArgoUML-FeatureLocation

Artifacts for the paper "Comparison-Based Feature Location in ArgoUML Variants" submitted as solution to the [ArgoUML feature location challenge](https://variability-challenges.github.io/2018/ArgoUMLSPL/index.html) of SPLC.

The [results](https://github.com/jku-isse/SPLC2019-Challenge-ArgoUML-FeatureLocation/tree/master/results) folder contains a subfolder for each of the 15 scenarios of the challenge.
Each scenario folder contains:
* the set of computed traces in the format requested by the challenge benchmark
* a CSV file with the metrics computed by the challenge benchmark
* a file `time.txt` containing the recorded runtimes per commit operation in milliseconds (one per line)
* a file `metrics.txt` containing only the total average precision, recall and F1 score metrics (separated by semicolon)

All that is needed to reproduce the results is available in two repositories:
* [ArgoUML challenge repository](https://github.com/but4reuse/argouml-spl-benchmark) contains the benchmark and the data set
* [ECCO repository](https://github.com/jku-isse/ecco/tree/develop) contains our solution including the [Java adapter implemented for the challenge](https://github.com/jku-isse/ecco/tree/develop/adapter/challenge).

The file [ChallengeTest.java](https://github.com/jku-isse/ecco/tree/develop/adapter/challenge/src/integrationTest/java/at/jku/isse/ecco/adapter/challenge/test/ChallengeTest.java) contains five unit test cases:
* `Do_All_Scenarios`: a convenience test case that executes the `Create_Repo`, `Compute_Results` and `Compute Metrics` test cases in this order for every scenario contained in the benchmark.
* `Create_Repo`: creates the ECCO repository containing all the computed traces for a specific scenario.
* `Compute_Results`: converts the traces stored in an ECCO repository to the format requested by the challenge benchmark.
* `Compute_Metrics`: computes the metrics requested by the challenge benchmark for computed results.
* `Analyze_Differences`: optional; shows all the differences between the results computed from an ECCO repository and the ground truth results provided by the challenge benchmark.
