# Recipe Execution Benchmark

This benchmark for recipe understanding in autonomous agents aims to support progressing the domain of natural language understanding by providing a setting in which performance can be measured on the everyday human activity of cooking. Showing deep understanding of such an activity requires both linguistic and extralinguistic skills, including reasoning with domain knowledge. For this goal, the benchmark provides a number of recipes written in natural (human) English that should be converted to a procedural semantic network of cooking operations that can be interpreted and executed by autonomous agents. A system, which supports one-click installation and execution, is also included that can perform recipe execution tasks in simulation allowing both analysis and evaluation of predicted networks. The provided evaluation metrics are mostly simulation-based, because demonstrating deep understanding of recipes can be done by effectively taking all the appropriate actions required for cooking the intended dish.

## website

Visit the recipe execution benchmark website at [https://ehai.ai.vub.ac.be/recipe-execution-benchmark/](https://ehai.ai.vub.ac.be/recipe-execution-benchmark/).

## data 

The directory [data](data) contains the recipe texts which are meant to serve as test input for developed natural language understanding models and the gold standard solutions which are their ideal output. In addition to the ideal semantic network, gold standard files have also been included that specify which sentence has led to certain cooking operations being included in the network. This has mostly been added to provide further insight when analyzing test results after development. Some example recipe texts with annotations and comments are provided in the [documentation](documentation) directory for use during development.  

The directory [metadata](metadata) contains the online sources of all recipe data, including the date on which they were retrieved.

## evaluation

The benchmark includes an evaluation script which will actually run the simulator and measure performance using the chosen metrics. These evaluation scripts are fully integrated in the [Babel toolkit](https://github.com/muhai-project/babel). More specifically, they can be found in the directory `applications/muhai-cookingbot`. 

To facilitate the evaluation, we also developed a standalone one-click executable. Due to file size limits, the executables could not be included in this repository. Instead, they are available for download via these links: [for Mac OS](https://ehai.vub.ac.be/recipe-execution-benchmark/assets/zips/cookingbot-evaluator-intel-mac.zip), [for Windows](https://ehai.vub.ac.be/recipe-execution-benchmark/assets/zips/cookingbot-evaluator-windows.zip), [for Linux](https://ehai.vub.ac.be/recipe-execution-benchmark/assets/zips/cookingbot-evaluator-linux.zip). More information about how to use this executable can be found in the [documentation](documentation) directory, including example solution files with explained result interpretations.

The directory [libs](libs) contains the Python library Smatch, which is required in case the executable should compute Smatch Score during evaluation. The path to this Smatch library should be given as a parameter to the executable. Again, more information about this is given in the [documentation](documentation). 

## documentation

The directory [documentation](documentation) contains extensive documentation on the primitive cooking operations that are used to form the semantic networks, the metrics and their interpretations, the gold standard solutions and how they are formed as well as how to actually use and possibly even extend the provided simulator. 

## citation

The recipe execution benchmark was published at LREC-COLING 2024:

```
@inproceedings{nevens2024benchmark,
    title = {A Benchmark for Recipe Understanding in Artificial Agents},
    author = {Jens Nevens and {De Haes}, Robin and Rachel Ringe and Mihai Pomarlan and Robert Porzel and Katrien Beuls and {Van Eecke}, Paul},
    year = 2024,
    pages = {22--42},
    booktitle = {Proceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation},
    venue = {Turin, Italy}
}
```

## acknowledgement

This research received funding from the EU’s H2020 RIA programme under grant agreement no. 951846 (MUHAI), the Research Foundation Flanders (FWO) through a post-doctoral grant awarded to PVE (grant no. 76929), and from the Collaborative Research Center (SFB) 1320 EASE – Everyday Activity Science and Engineering, University of Bremen (www.ease-crc.org), sub-project P01 "Embodied Semantics for the Language of Action and Change".